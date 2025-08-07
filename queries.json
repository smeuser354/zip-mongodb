
db.zips.find({ city: "NEW YORK" });

db.zips.find({ state: "CA" }).limit(100);

db.zips.find({ pop: { $gt: 50000 } });

db.zips.find({ loc: { $near: [‑86.5, 33.6] } });

db.zips.aggregate([ { $group: { _id: "$state", totalPop: { $sum: "$pop" } } } ]);

db.zips.aggregate([ { $project: { city: 1, pop: 1 } }, { $sort: { pop: -1 } } ]);

db.zips.find({ city: /^A/ });

db.zips.aggregate([ { $match: { state: "NY" } }, { $group: { _id: "$city", postal_codes: { $addToSet: "$_id" } } } ]);

db.zips.find({ state: "TX", pop: { $lt: 1000 } });

db.zips.aggregate([ { $match: { city: "LAKEWOOD" } }, { $group: { _id: "$state", avgPop: { $avg: "$pop" } } } ]);
