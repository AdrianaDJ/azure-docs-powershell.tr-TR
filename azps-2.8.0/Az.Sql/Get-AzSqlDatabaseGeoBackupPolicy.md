---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 97373d35cee4efb80ca2953c0085fe6b153ea138
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933673"
---
# <span data-ttu-id="24236-101">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="24236-101">Get-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="24236-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24236-102">SYNOPSIS</span></span>
<span data-ttu-id="24236-103">Bir veritabanı coğrafi yedekleme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="24236-103">Gets a database geo backup policy.</span></span>

## <span data-ttu-id="24236-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24236-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24236-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="24236-105">DESCRIPTION</span></span>
<span data-ttu-id="24236-106">**Get-AzSqlDatabaseGeoBackupPolicy** cmdlet 'i, bu veritabanına kaydedilen coğrafi yedekleme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="24236-106">The **Get-AzSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="24236-107">Bu, yedek depolama ilkesini tanımlamak için kullanılan bir Azure yedekleme kaynağı.</span><span class="sxs-lookup"><span data-stu-id="24236-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="24236-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24236-108">EXAMPLES</span></span>

## <span data-ttu-id="24236-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24236-109">PARAMETERS</span></span>

### <span data-ttu-id="24236-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="24236-110">-DatabaseName</span></span>
<span data-ttu-id="24236-111">Bu cmdlet 'in coğrafi yedekleme ilkesini aldığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24236-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

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

### <span data-ttu-id="24236-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24236-112">-DefaultProfile</span></span>
<span data-ttu-id="24236-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="24236-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24236-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24236-114">-ResourceGroupName</span></span>
<span data-ttu-id="24236-115">Bu veritabanını içeren sunucunun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24236-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="24236-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="24236-116">-ServerName</span></span>
<span data-ttu-id="24236-117">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24236-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="24236-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24236-118">CommonParameters</span></span>
<span data-ttu-id="24236-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24236-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24236-120">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="24236-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24236-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24236-121">INPUTS</span></span>

### <span data-ttu-id="24236-122">System. String</span><span class="sxs-lookup"><span data-stu-id="24236-122">System.String</span></span>

## <span data-ttu-id="24236-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24236-123">OUTPUTS</span></span>

### <span data-ttu-id="24236-124">Microsoft. Azure. Commands. Sql. Backup. model. Azuressqldatabasegeobackuppolicymodel</span><span class="sxs-lookup"><span data-stu-id="24236-124">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="24236-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24236-125">NOTES</span></span>

## <span data-ttu-id="24236-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24236-126">RELATED LINKS</span></span>

[<span data-ttu-id="24236-127">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="24236-127">Set-AzSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="24236-128">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="24236-128">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
