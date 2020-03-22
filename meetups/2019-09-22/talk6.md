#Fast interactive object annotation with curve-gcn
## Huan Ling

Using ai to accelerate data labeling,

A human creates the bounding box and selects if the segmentations should be a polygon or a contour, the ai then predicts the object boundary, the human fixes any problems and another ai uses that as new data and predicts the curve another time

Image > cnn + boundary prediction > image + initialized boundary > boundary refinement

PSP-Deeplab

The ai that does the corrections after the human input only corrects neighbouring points


