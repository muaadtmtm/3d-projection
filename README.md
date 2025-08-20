# Projections 3D de l’action naturelle des sous-groupes finis du groupe spécial orthogonal sur des polytopes uniformes de dimension 2n

Ce projet illustre, par des animations Blender, la projection en 3D de l’action de sous-groupes finis de SO(2n) sur des **polytopes uniformes** (simplexes, hypercubes/orthoplexes, demicubes, 24-cell, 120-/600-cell, versions rectifiées/stellées, etc.).  
Le script Python génère les sommets via permutations de coordonnées (SymPy) et changements de signes, reconstruit l’**adjacence** par détection d’arêtes (seuil sur la distance), échantillonne une **base orthonormée 3D** via une matrice de SO(d) (SciPy), projette, puis **anime** une rotation bloc-diagonale (plans 2×2) en insérant des keyframes (sphères = sommets, cylindres = arêtes).

**Liens rapides**  
- 🎞️ **Galerie live** : https://muaadtmtm.github.io/3d-projection/  
- 📓 **Notebook** : [`notebooks/3D_Projection.ipynb`](notebooks/3D_Projection.ipynb)  
- 🧾 **README brut** : [`docs/index.md`](docs/index.md) (page de la galerie)  
- 🛠️ **Code source** : https://github.com/muaadtmtm/3d-projection

---

## Gallery (cliquer sur un aperçu pour ouvrir la vidéo)

<table>
<tr>
<td align="center">
  <a href="https://muaadtmtm.github.io/3d-projection/videos/4-orthoplexe.mp4">
    <img src="https://muaadtmtm.github.io/3d-projection/assets/4-orthoplexe.gif" width="220" alt="4-orthoplexe"/>
    <br/><sub><code>4-orthoplexe.mp4</code></sub>
  </a>
</td>
<td align="center">
  <a href="https://muaadtmtm.github.io/3d-projection/videos/4-simplexe.mp4">
    <img src="https://muaadtmtm.github.io/3d-projection/assets/4-simplexe.gif" width="220" alt="4-simplexe"/>
    <br/><sub><code>4-simplexe.mp4</code></sub>
  </a>
</td>
<td align="center">
  <a href="https://muaadtmtm.github.io/3d-projection/videos/6-simplexe.mp4">
    <img src="https://muaadtmtm.github.io/3d-projection/assets/6-simplexe.gif" width="220" alt="6-simplexe"/>
    <br/><sub><code>6-simplexe.mp4</code></sub>
  </a>
</td>
</tr>

<tr>
<td align="center">
  <a href="https://muaadtmtm.github.io/3d-projection/videos/8-demicube.mp4">
    <img src="https://muaadtmtm.github.io/3d-projection/assets/8-demicube.gif" width="220" alt="8-demicube"/>
    <br/><sub><code>8-demicube.mp4</code></sub>
  </a>
</td>
<td align="center">
  <a href="https://muaadtmtm.github.io/3d-projection/videos/8-orthoplexe.mp4">
    <img src="https://muaadtmtm.github.io/3d-projection/assets/8-orthoplexe.gif" width="220" alt="8-orthoplexe"/>
    <br/><sub><code>8-orthoplexe.mp4</code></sub>
  </a>
</td>
<td align="center">
  <a href="https://muaadtmtm.github.io/3d-projection/videos/8-simplexe.mp4">
    <img src="https://muaadtmtm.github.io/3d-projection/assets/8-simplexe.gif" width="220" alt="8-simplexe"/>
    <br/><sub><code>8-simplexe.mp4</code></sub>
  </a>
</td>
</tr>

<tr>
<td align="center">
  <a href="https://muaadtmtm.github.io/3d-projection/videos/10-simplexe.mp4">
    <img src="https://muaadtmtm.github.io/3d-projection/assets/10-simplexe.gif" width="220" alt="10-simplexe"/>
    <br/><sub><code>10-simplexe.mp4</code></sub>
  </a>
</td>
<td align="center">
  <a href="https://muaadtmtm.github.io/3d-projection/videos/24-cell.mp4">
    <img src="https://muaadtmtm.github.io/3d-projection/assets/24-cell.gif" width="220" alt="24-cell"/>
    <br/><sub><code>24-cell.mp4</code></sub>
  </a>
</td>
<td align="center">
  <a href="https://muaadtmtm.github.io/3d-projection/videos/120-cell.mp4">
    <img src="https://muaadtmtm.github.io/3d-projection/assets/120-cell.gif" width="220" alt="120-cell"/>
    <br/><sub><code>120-cell.mp4</code></sub>
  </a>
</td>
</tr>

<tr>
<td align="center">
  <a href="https://muaadtmtm.github.io/3d-projection/videos/600-cell.mp4">
    <img src="https://muaadtmtm.github.io/3d-projection/assets/600-cell.gif" width="220" alt="600-cell"/>
    <br/><sub><code>600-cell.mp4</code></sub>
  </a>
</td>
<td align="center">
  <a href="https://muaadtmtm.github.io/3d-projection/videos/great_grand_stellated_120-cell.mp4">
    <img src="https://muaadtmtm.github.io/3d-projection/assets/great_grand_stellated_120-cell.gif" width="220" alt="great_grand_stellated_120-cell"/>
    <br/><sub><code>great_grand_stellated_120-cell.mp4</code></sub>
  </a>
</td>
<td align="center">
  <a href="https://muaadtmtm.github.io/3d-projection/videos/great_stellated_120-cell.mp4">
    <img src="https://muaadtmtm.github.io/3d-projection/assets/great_stellated_120-cell.gif" width="220" alt="great_stellated_120-cell"/>
    <br/><sub><code>great_stellated_120-cell.mp4</code></sub>
  </a>
</td>
</tr>

<tr>
<td align="center">
  <a href="https://muaadtmtm.github.io/3d-projection/videos/hypercube.mp4">
    <img src="https://muaadtmtm.github.io/3d-projection/assets/hypercube.gif" width="220" alt="hypercube"/>
    <br/><sub><code>hypercube.mp4</code></sub>
  </a>
</td>
<td align="center">
  <a href="https://muaadtmtm.github.io/3d-projection/videos/rectified_6-cube.mp4">
    <img src="https://muaadtmtm.github.io/3d-projection/assets/rectified_6-cube.gif" width="220" alt="rectified_6-cube"/>
    <br/><sub><code>rectified_6-cube.mp4</code></sub>
  </a>
</td>
<td align="center">
  <a href="https://muaadtmtm.github.io/3d-projection/videos/small_stellated_120-cell.mp4">
    <img src="https://muaadtmtm.github.io/3d-projection/assets/small_stellated_120-cell.gif" width="220" alt="small_stellated_120-cell"/>
    <br/><sub><code>small_stellated_120-cell.mp4</code></sub>
  </a>
</td>
</tr>
</table>

---