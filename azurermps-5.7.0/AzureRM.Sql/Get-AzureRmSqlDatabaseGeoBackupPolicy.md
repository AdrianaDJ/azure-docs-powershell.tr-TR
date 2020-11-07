---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 2e5e313fe35770e6841909e1f0718cfe3d9c8664
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763210"
---
# <span data-ttu-id="40fc6-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="40fc6-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="40fc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="40fc6-103">Bir veritabanı coğrafi yedekleme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="40fc6-103">Gets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40fc6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40fc6-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40fc6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="40fc6-105">DESCRIPTION</span></span>
<span data-ttu-id="40fc6-106">**Get-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet 'i, bu veritabanına kaydedilen coğrafi yedekleme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="40fc6-106">The **Get-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="40fc6-107">Bu, yedek depolama ilkesini tanımlamak için kullanılan bir Azure yedekleme kaynağı.</span><span class="sxs-lookup"><span data-stu-id="40fc6-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="40fc6-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40fc6-108">EXAMPLES</span></span>

## <span data-ttu-id="40fc6-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40fc6-109">PARAMETERS</span></span>

### <span data-ttu-id="40fc6-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="40fc6-110">-DatabaseName</span></span>
<span data-ttu-id="40fc6-111">Bu cmdlet 'in coğrafi yedekleme ilkesini aldığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="40fc6-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40fc6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40fc6-112">-DefaultProfile</span></span>
<span data-ttu-id="40fc6-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="40fc6-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40fc6-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40fc6-114">-ResourceGroupName</span></span>
<span data-ttu-id="40fc6-115">Bu veritabanını içeren sunucunun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="40fc6-115">Specifies the name of the resource group of the server that contains this database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40fc6-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="40fc6-116">-ServerName</span></span>
<span data-ttu-id="40fc6-117">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="40fc6-117">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40fc6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40fc6-118">CommonParameters</span></span>
<span data-ttu-id="40fc6-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40fc6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40fc6-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40fc6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40fc6-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40fc6-121">INPUTS</span></span>

### <span data-ttu-id="40fc6-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="40fc6-122">None</span></span>
<span data-ttu-id="40fc6-123">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="40fc6-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="40fc6-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40fc6-124">OUTPUTS</span></span>

## <span data-ttu-id="40fc6-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40fc6-125">NOTES</span></span>

## <span data-ttu-id="40fc6-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40fc6-126">RELATED LINKS</span></span>

[<span data-ttu-id="40fc6-127">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="40fc6-127">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="40fc6-128">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="40fc6-128">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
