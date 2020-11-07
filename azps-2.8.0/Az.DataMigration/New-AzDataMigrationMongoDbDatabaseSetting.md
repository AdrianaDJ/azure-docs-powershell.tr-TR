---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: d05b6507ea8e1d5244e23ab7b8b6222848a1d088
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752245"
---
# <span data-ttu-id="79763-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="79763-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="79763-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79763-102">SYNOPSIS</span></span>
<span data-ttu-id="79763-103">MongoDb geçişi için geçiş için veritabanı ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="79763-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="79763-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79763-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="79763-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="79763-105">DESCRIPTION</span></span>
<span data-ttu-id="79763-106">New-AzDataMigrationMongoDbDatabaseSetting cmdlet 'i, işleme ve silme davranışını belirten geçiş ayarı nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="79763-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="79763-107">Çıkış, koleksiyonun adına ve geçiş görevini çağırmaya kullanılabilen ayarın değerine sahip bir anahtar değeri çiftidir.</span><span class="sxs-lookup"><span data-stu-id="79763-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="79763-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79763-108">EXAMPLES</span></span>

### <span data-ttu-id="79763-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="79763-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="79763-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79763-110">PARAMETERS</span></span>

### <span data-ttu-id="79763-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="79763-111">-Name</span></span>
<span data-ttu-id="79763-112">Veritabanının adı</span><span class="sxs-lookup"><span data-stu-id="79763-112">Name of the database</span></span>

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
### <span data-ttu-id="79763-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="79763-113">-TargetRequestUnit</span></span>
<span data-ttu-id="79763-114">Adanmış veritabanı düzeyi istek birim değeri.</span><span class="sxs-lookup"><span data-stu-id="79763-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="79763-115">Ayarlanmamışsa, bu koleksiyon paylaşılan veritabanı RU kullanır.</span><span class="sxs-lookup"><span data-stu-id="79763-115">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="79763-116">-Koleksiyonlar</span><span class="sxs-lookup"><span data-stu-id="79763-116">-Collections</span></span>
<span data-ttu-id="79763-117">New-AzureRmDmsMongoDbDatabaseSetting çağrısı tarafından döndürülen MongoDb koleksiyon ayarı nesneleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="79763-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

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

### <span data-ttu-id="79763-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79763-118">CommonParameters</span></span>
<span data-ttu-id="79763-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79763-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79763-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79763-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79763-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79763-121">INPUTS</span></span>

### <span data-ttu-id="79763-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="79763-122">None</span></span>

## <span data-ttu-id="79763-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79763-123">OUTPUTS</span></span>

### <span data-ttu-id="79763-124">Microsoft. Azure. Commands. DataMigration. modeller. MongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="79763-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="79763-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79763-125">NOTES</span></span>

## <span data-ttu-id="79763-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79763-126">RELATED LINKS</span></span>
