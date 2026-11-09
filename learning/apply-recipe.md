# Apply recipe: DRAFT, not locked (Nov 8, 2026)

Owner: "You need to… hold them with two fingers, like pinching them as you put the patch on." This draft becomes LOCKED only after a Gemini test passes the frame-by-frame check and the owner approves it, the same way `peel-recipe.md` was locked. Background: `learning/prompting-research.md`.

## Rules
1. **The grip is in the still.** Thumb and index fingertips pinch the patch's outer edge; the other fingers are loosely curled. The patch hangs free from the pinch, with its sticky side toward her face. Her palm faces down or toward the camera side and never touches the patch. Use one hand for the small pieces. The forehead band uses two hands, one pinching each end.
2. **Light:** front light from the camera side; hand and face share the same light and tone. Hold the hand a hand's width in front of her face, never near the lens.
3. **One action per clip,** in this order, each a separate clip, using the best 1–3 s of each:
   1. Bring the patch in: from a hand's width away to just touching the skin.
   2. Press it on: the pinch opens, and the index fingertip then the middle fingertip press along the patch from one end to the other.
   3. Smooth: two fingertips glide once along it, then rest.
4. **Slow and steady, with an end point.** Every clip ends on a held still pose.
5. **End frame for clip 1 only (to test):** the same image edited so the patch is on the skin with the fingertips still pinching the edge. Make it with Nano Banana by editing the start still, never as a new image.
6. Motion goes first and stays short. The PATCHES block follows word for word. Negatives last, 3–5 named defects.

## Still prompt (S_APPLY_PINCH, edit the cast still)
> CHANGES ONLY: she holds one clear under-eye crescent patch a hand's width in front of her face, at cheek height on the frame-right side. Her thumb and index fingertip pinch only its outer tip; her other three fingers are loosely curled; the patch hangs free from the pinch, its sticky side facing her cheek, and no other part of her hand touches it. Her fingertips and nails are clearly visible and separate. Her eyes are open, looking at the patch in a small mirror just off camera [or: toward the lens]. Her hand is lit by the same soft front light as her face and has the same skin tone. Exactly two hands, five fingers each. [PATCHES block verbatim; only the pieces she holds or wears exist.]

## Clip 1 prompt (bring and place, about 4–5 s)
> Static locked-off phone camera. Her hand, which pinches the patch's outer tip between thumb and index finger, slowly and steadily moves the patch toward her face and lays its inner end on the skin just below her lower lashes; the pinch keeps holding the outer tip the whole time; then her hand stays still. Her face and head stay still, eyes open. The light on her hand never changes and matches her face. [PATCHES block.] Avoid: fingers flat against the patch, patch stuck to the palm, extra or fused fingers, white glare spots on the patch.

## Clip 2 prompt (press on, about 3–4 s)
> Static locked-off phone camera. Her thumb lets go of the patch's tip; her index fingertip gently presses along the patch from the inner end to the outer end in one slow, even stroke, the clear patch settling flat onto her skin as the finger passes; then her finger lifts a few centimetres away and rests. [PATCHES block.] Avoid: patch folding, patch sliding, extra or fused fingers, white glare spots.

## Open questions for the test
- Does Gemini/Omni keep the pinch for the whole clip from the still alone, or does it need the end frame?
- Under-eye crescent vs forehead band: test the under-eye piece first (one hand, smaller move).
