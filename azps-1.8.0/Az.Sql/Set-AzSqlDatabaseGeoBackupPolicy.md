---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 6ac39ae2daba5f97b9046f3860eb34d3bb0f03ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758792"
---
# <span data-ttu-id="5c3fa-101">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="5c3fa-101">Set-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="5c3fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c3fa-102">SYNOPSIS</span></span>
<span data-ttu-id="5c3fa-103">Bir veritabanı coğrafi yedekleme ilkesi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5c3fa-103">Sets a database geo backup policy.</span></span>

## <span data-ttu-id="5c3fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c3fa-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5c3fa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c3fa-105">DESCRIPTION</span></span>
<span data-ttu-id="5c3fa-106">**Set-AzSqlDatabaseGeoBackupPolicy** cmdlet 'i veritabanına kaydedilen coğrafi yedekleme ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5c3fa-106">The **Set-AzSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="5c3fa-107">Bu, yedek depolama ilkesini tanımlamak için kullanılan bir Azure yedekleme kaynağı.</span><span class="sxs-lookup"><span data-stu-id="5c3fa-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="5c3fa-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c3fa-108">EXAMPLES</span></span>

## <span data-ttu-id="5c3fa-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c3fa-109">PARAMETERS</span></span>

### <span data-ttu-id="5c3fa-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5c3fa-110">-DatabaseName</span></span>
<span data-ttu-id="5c3fa-111">Bu cmdlet 'in coğrafi yedekleme ilkesini ayarladığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c3fa-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="5c3fa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c3fa-112">-DefaultProfile</span></span>
<span data-ttu-id="5c3fa-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5c3fa-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c3fa-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c3fa-114">-ResourceGroupName</span></span>
<span data-ttu-id="5c3fa-115">Bu veritabanını içeren sunucunun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c3fa-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="5c3fa-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5c3fa-116">-ServerName</span></span>
<span data-ttu-id="5c3fa-117">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c3fa-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="5c3fa-118">Durumlu</span><span class="sxs-lookup"><span data-stu-id="5c3fa-118">-State</span></span>
<span data-ttu-id="5c3fa-119">Coğrafi yedekleme ilkesinin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c3fa-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="5c3fa-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5c3fa-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5c3fa-121">Etkin</span><span class="sxs-lookup"><span data-stu-id="5c3fa-121">Enabled</span></span> 
- <span data-ttu-id="5c3fa-122">DISABLED</span><span class="sxs-lookup"><span data-stu-id="5c3fa-122">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel+GeoBackupPolicyState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c3fa-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="5c3fa-123">-Confirm</span></span>
<span data-ttu-id="5c3fa-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5c3fa-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c3fa-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c3fa-125">-WhatIf</span></span>
<span data-ttu-id="5c3fa-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c3fa-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c3fa-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5c3fa-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c3fa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c3fa-128">CommonParameters</span></span>
<span data-ttu-id="5c3fa-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c3fa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c3fa-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5c3fa-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c3fa-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c3fa-131">INPUTS</span></span>

### <span data-ttu-id="5c3fa-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5c3fa-132">System.String</span></span>

## <span data-ttu-id="5c3fa-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c3fa-133">OUTPUTS</span></span>

### <span data-ttu-id="5c3fa-134">Microsoft. Azure. Commands. Sql. Backup. model. Azuressqldatabasegeobackuppolicymodel</span><span class="sxs-lookup"><span data-stu-id="5c3fa-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="5c3fa-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c3fa-135">NOTES</span></span>

## <span data-ttu-id="5c3fa-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c3fa-136">RELATED LINKS</span></span>

[<span data-ttu-id="5c3fa-137">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="5c3fa-137">Get-AzSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="5c3fa-138">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="5c3fa-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

