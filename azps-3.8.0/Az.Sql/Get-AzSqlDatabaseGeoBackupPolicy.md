---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: d69d6c2976e71183fed07e2c18adc730d8ea6e61
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097024"
---
# <span data-ttu-id="86ef9-101">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="86ef9-101">Get-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="86ef9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86ef9-102">SYNOPSIS</span></span>
<span data-ttu-id="86ef9-103">Bir veritabanı coğrafi yedekleme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="86ef9-103">Gets a database geo backup policy.</span></span>

## <span data-ttu-id="86ef9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="86ef9-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86ef9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="86ef9-105">DESCRIPTION</span></span>
<span data-ttu-id="86ef9-106">**Get-AzSqlDatabaseGeoBackupPolicy** cmdlet 'i, bu veritabanına kaydedilen coğrafi yedekleme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="86ef9-106">The **Get-AzSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="86ef9-107">Bu, yedek depolama ilkesini tanımlamak için kullanılan bir Azure yedekleme kaynağı.</span><span class="sxs-lookup"><span data-stu-id="86ef9-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="86ef9-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="86ef9-108">EXAMPLES</span></span>

## <span data-ttu-id="86ef9-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="86ef9-109">PARAMETERS</span></span>

### <span data-ttu-id="86ef9-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="86ef9-110">-DatabaseName</span></span>
<span data-ttu-id="86ef9-111">Bu cmdlet 'in coğrafi yedekleme ilkesini aldığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="86ef9-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ef9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86ef9-112">-DefaultProfile</span></span>
<span data-ttu-id="86ef9-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="86ef9-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ef9-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86ef9-114">-ResourceGroupName</span></span>
<span data-ttu-id="86ef9-115">Bu veritabanını içeren sunucunun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="86ef9-115">Specifies the name of the resource group of the server that contains this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ef9-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="86ef9-116">-ServerName</span></span>
<span data-ttu-id="86ef9-117">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="86ef9-117">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ef9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86ef9-118">CommonParameters</span></span>
<span data-ttu-id="86ef9-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="86ef9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86ef9-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="86ef9-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86ef9-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="86ef9-121">INPUTS</span></span>

### <span data-ttu-id="86ef9-122">System. String</span><span class="sxs-lookup"><span data-stu-id="86ef9-122">System.String</span></span>

## <span data-ttu-id="86ef9-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="86ef9-123">OUTPUTS</span></span>

### <span data-ttu-id="86ef9-124">Microsoft. Azure. Commands. Sql. Backup. model. Azuressqldatabasegeobackuppolicymodel</span><span class="sxs-lookup"><span data-stu-id="86ef9-124">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="86ef9-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="86ef9-125">NOTES</span></span>

## <span data-ttu-id="86ef9-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="86ef9-126">RELATED LINKS</span></span>

[<span data-ttu-id="86ef9-127">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="86ef9-127">Set-AzSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="86ef9-128">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="86ef9-128">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
