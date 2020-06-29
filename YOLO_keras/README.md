# YOLO

### Key concepts

Non-max suppression (NMS):

- make sure that your algorithm detects each object only once
- output the maximal probabilities classifications but suppress the close-by ones with high IOU

Anchor box:

- enables detection of overlapping objects by associating multiple objects to their respective anchor boxes.
- Each object is assigned to the grid cell that contains the midpoint and anchor box for the grid cell with the higest IoU.

Region proposal:

- Run segmentation first and then run classification on the blobs
