---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 4e0082d742aff54ba4d4b57d4e148e249ab8ecf7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320433"
---
# <span data-ttu-id="91ba3-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="91ba3-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="91ba3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91ba3-102">SYNOPSIS</span></span>
<span data-ttu-id="91ba3-103">MongoDb geçişine göre geçiş için koleksiyon ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="91ba3-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="91ba3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91ba3-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="91ba3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="91ba3-105">DESCRIPTION</span></span>
<span data-ttu-id="91ba3-106">New-AzDataMigrationMongoDbCollectionSetting cmdlet 'i, işleme ve silme davranışını belirten geçiş ayarı nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="91ba3-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="91ba3-107">Derleme, koleksiyonun adı ve ayarın değeri olan anahtar değer çiftine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="91ba3-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="91ba3-108">Çıktı, geçiş için veritabanı düzeyi ayarlarının montajı sırasında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="91ba3-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="91ba3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91ba3-109">EXAMPLES</span></span>

### <span data-ttu-id="91ba3-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="91ba3-110">Example 1</span></span>
```
PS C:\> $x = New-AzDataMigrationMongoDbCollectionSetting -Name myCollection -TargetRequestUnit 1000 -CanDelete -ShardKey "_id:-1,age:1,name"
PS C:\> $x

Name         Setting
----         -------
myCollection Microsoft.Azure.Management.DataMigration.Models.MongoDbCollectionSettings

PS C:\> $x.Setting

CanDelete ShardKey                                                               TargetRUs
--------- --------                                                               ---------
     True Microsoft.Azure.Management.DataMigration.Models.MongoDbShardKeySetting      1000

```

## <span data-ttu-id="91ba3-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91ba3-111">PARAMETERS</span></span>

### <span data-ttu-id="91ba3-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="91ba3-112">-Name</span></span>
<span data-ttu-id="91ba3-113">Koleksiyonun adı</span><span class="sxs-lookup"><span data-stu-id="91ba3-113">Name of the collection</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ba3-114">-Shardanahtarı</span><span class="sxs-lookup"><span data-stu-id="91ba3-114">-ShardKey</span></span>
<span data-ttu-id="91ba3-115">Shard anahtarlarının virgülle ayrılmış listesi.</span><span class="sxs-lookup"><span data-stu-id="91ba3-115">The comma separated list of the shard keys.</span></span> <span data-ttu-id="91ba3-116">MongoDb hedefi için, "_id, e-posta:-1" gibi bir sıra, "ShardKeyName: Order" ifadesini</span><span class="sxs-lookup"><span data-stu-id="91ba3-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ba3-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="91ba3-117">-TargetRequestUnit</span></span>
<span data-ttu-id="91ba3-118">Adanmış koleksiyon isteği birim değeri.</span><span class="sxs-lookup"><span data-stu-id="91ba3-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="91ba3-119">Ayarlanmamışsa, bu koleksiyon paylaşılan veritabanı RU kullanır.</span><span class="sxs-lookup"><span data-stu-id="91ba3-119">If not set, that collection uses shared database RU.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: RU

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ba3-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="91ba3-120">-CanDelete</span></span>
<span data-ttu-id="91ba3-121">Hedef verilerin silinip silinmeyeceği beklenen bir anahtar ayarlıysa, geçiş sırasında temizlenir</span><span class="sxs-lookup"><span data-stu-id="91ba3-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="91ba3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91ba3-122">CommonParameters</span></span>
<span data-ttu-id="91ba3-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91ba3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91ba3-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91ba3-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91ba3-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91ba3-125">INPUTS</span></span>

### <span data-ttu-id="91ba3-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="91ba3-126">None</span></span>

## <span data-ttu-id="91ba3-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91ba3-127">OUTPUTS</span></span>

### <span data-ttu-id="91ba3-128">Microsoft. Azure. Commands. DataMigration. modeller. MongoDbCollectionSetting></span><span class="sxs-lookup"><span data-stu-id="91ba3-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="91ba3-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91ba3-129">NOTES</span></span>

## <span data-ttu-id="91ba3-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91ba3-130">RELATED LINKS</span></span>
