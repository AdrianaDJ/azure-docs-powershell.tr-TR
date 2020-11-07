---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: 9ae50501306dfa1a76fa4966113ac2e9b681f6c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937391"
---
# <span data-ttu-id="757ee-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="757ee-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="757ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="757ee-102">SYNOPSIS</span></span>
<span data-ttu-id="757ee-103">MongoDb geçişi için geçiş için veritabanı ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="757ee-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="757ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="757ee-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="757ee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="757ee-105">DESCRIPTION</span></span>
<span data-ttu-id="757ee-106">New-AzDataMigrationMongoDbDatabaseSetting cmdlet 'i, işleme ve silme davranışını belirten geçiş ayarı nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="757ee-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="757ee-107">Çıkış, koleksiyonun adına ve geçiş görevini çağırmaya kullanılabilen ayarın değerine sahip bir anahtar değeri çiftidir.</span><span class="sxs-lookup"><span data-stu-id="757ee-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="757ee-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="757ee-108">EXAMPLES</span></span>

### <span data-ttu-id="757ee-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="757ee-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="757ee-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="757ee-110">PARAMETERS</span></span>

### <span data-ttu-id="757ee-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="757ee-111">-Name</span></span>
<span data-ttu-id="757ee-112">Veritabanının adı</span><span class="sxs-lookup"><span data-stu-id="757ee-112">Name of the database</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="757ee-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="757ee-113">-TargetRequestUnit</span></span>
<span data-ttu-id="757ee-114">Adanmış veritabanı düzeyi istek birim değeri.</span><span class="sxs-lookup"><span data-stu-id="757ee-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="757ee-115">Ayarlanmamışsa, bu koleksiyon paylaşılan veritabanı RU kullanır.</span><span class="sxs-lookup"><span data-stu-id="757ee-115">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="757ee-116">-Koleksiyonlar</span><span class="sxs-lookup"><span data-stu-id="757ee-116">-Collections</span></span>
<span data-ttu-id="757ee-117">New-AzureRmDmsMongoDbDatabaseSetting çağrısı tarafından döndürülen MongoDb koleksiyon ayarı nesneleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="757ee-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

```yaml
Type: System.Collections.Generic.KeyValuePair<string, MongoDbCollectionSettings>[]
Parameter Sets: (All)
Aliases: colls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757ee-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="757ee-118">CommonParameters</span></span>
<span data-ttu-id="757ee-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="757ee-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="757ee-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="757ee-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="757ee-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="757ee-121">INPUTS</span></span>

### <span data-ttu-id="757ee-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="757ee-122">None</span></span>

## <span data-ttu-id="757ee-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="757ee-123">OUTPUTS</span></span>

### <span data-ttu-id="757ee-124">Microsoft. Azure. Commands. DataMigration. modeller. MongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="757ee-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="757ee-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="757ee-125">NOTES</span></span>

## <span data-ttu-id="757ee-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="757ee-126">RELATED LINKS</span></span>
