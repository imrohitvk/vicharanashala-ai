# Adding your photo to the Team page

You don't need to edit any code. Upload **one image file with your name on it**, and
your card on the Team page picks it up by itself.

## 1. Prepare the photo

- A **square** head-and-shoulders photo works best. It is shown as a small circle.
- **JPG**, at least **400 × 400 pixels**, and **under 300 KB**. A phone photo straight
  off the camera is usually 3–5 MB, so shrink it first (for example with
  squoosh.app, or "Resize" in Preview on a Mac).
- **Name the file exactly as in the table below**, all lowercase, words joined with
  hyphens — the same pattern as the photos already uploaded.

| Person | File name | Uploaded? |
|---|---|---|
| Prof. Sudarshan Iyengar | `s-r-s-iyengar.jpg` | yes |
| Aditya BMV | `aditya-bmv.jpg` | |
| Jinal Gupta | `jinal-gupta.jpg` | yes |
| Meenakshi V | `meenakshi-v.jpg` | |
| Nakul Pise | `nakul-pise.png` | yes |
| Dr. Pavani Ayinampudi | `pavani-ayinampudi.jpg` | yes |
| Prakash Hegade | `prakash-hegade.jpg` | |
| Rohit Sharma | `rohit-sharma.jpg` | |
| Sakshi Sharma | `sakshi-sharma.jpg` | |
| Shivam Gurjar | `shivam-gurjar.png` | yes |
| Atul | `atul.jpg` | |
| Harshdeep | `harshdeep.jpg` | |
| Meenakshi Kalotra | `meenakshi-kalotra.jpg` | |
| Rajan Gupta | `rajan-gupta.jpg` | |

`.jpeg`, `.png` and `.webp` also work, as long as the part before the dot matches.

**Already in the folder but with no card on the page yet:** `krishna-gelra.jpg`,
`mudit-agrawal.jpg`, `s-hamsalekha.jpg`. Those people need a card added first (see
the last section below) — the photo will then show on its own.

## 2. Upload it as a pull request (in the browser)

1. Sign in to GitHub and open
   **github.com/vicharanashala/vicharanashala-ai/tree/main/assets/images/team**
2. Click **Add file → Upload files** and drop in your photo.
3. GitHub will say you don't have write access and offer to make a copy (a "fork")
   for you. Accept. That's normal.
4. Write a short message such as *"Add Rohit's team photo"* and click
   **Propose changes**, then **Create pull request**.
5. Someone with access to the lab repo reviews and merges it. The photo appears on
   the live site a few minutes later.

Each person uploads their own file, so several people can do this at the same time
without getting in each other's way.

## Someone new joining the team?

A new person needs a card first — that one does need an edit to `team-members.md`
(copy an existing card and change the name). Put
`{% include team-photo.html name="their-name" alt="Their Name" %}` where the
photo goes, and add them to the table above.
