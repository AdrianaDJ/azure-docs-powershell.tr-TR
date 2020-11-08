---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 2e98f832bd13509a853d85037a413b6fd5895695
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098674"
---
# <span data-ttu-id="63693-101">Remove-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="63693-101">Remove-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="63693-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63693-102">SYNOPSIS</span></span>
<span data-ttu-id="63693-103">Bir SQL veritabanından geri yükleme noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="63693-103">Removes given restore point from a SQL Database.</span></span>

## <span data-ttu-id="63693-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63693-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63693-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="63693-105">DESCRIPTION</span></span>
<span data-ttu-id="63693-106">**Remove-AzSqlDatabaseRestorePoint** cmdlet 'ı Azure SQL veritabanından geri yükleme noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="63693-106">The **Remove-AzSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>
<span data-ttu-id="63693-107">Bu cmdlet Şu anda Azure SQL veritabanında SQL Server DataWarehouse hizmeti tarafından desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="63693-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="63693-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63693-108">EXAMPLES</span></span>

### <span data-ttu-id="63693-109">Örnek 1: geri yükleme noktasını kaldırır</span><span class="sxs-lookup"><span data-stu-id="63693-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="63693-110">Bu komut, Azure SQL veritabanı 'nın oluşturma tarihi için geri yükleme noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="63693-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="63693-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63693-111">PARAMETERS</span></span>

### <span data-ttu-id="63693-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="63693-112">-DatabaseName</span></span>
<span data-ttu-id="63693-113">SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63693-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="63693-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63693-114">-DefaultProfile</span></span>
<span data-ttu-id="63693-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="63693-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63693-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="63693-116">-PassThru</span></span>
<span data-ttu-id="63693-117">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="63693-117">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63693-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63693-118">-ResourceGroupName</span></span>
<span data-ttu-id="63693-119">SQL veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63693-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="63693-120">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="63693-120">-RestorePointCreationDate</span></span>
<span data-ttu-id="63693-121">Geri yükleme noktası oluşturma tarihini belirtir.</span><span class="sxs-lookup"><span data-stu-id="63693-121">Specifies the restore point creation date.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63693-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="63693-122">-ServerName</span></span>
<span data-ttu-id="63693-123">Veritabanını barındıran AzureSQL sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63693-123">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="63693-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="63693-124">-Confirm</span></span>
<span data-ttu-id="63693-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="63693-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63693-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63693-126">-WhatIf</span></span>
<span data-ttu-id="63693-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="63693-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63693-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="63693-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63693-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63693-129">CommonParameters</span></span>
<span data-ttu-id="63693-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63693-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63693-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="63693-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63693-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63693-132">INPUTS</span></span>

### <span data-ttu-id="63693-133">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="63693-133">System.DateTime</span></span>

### <span data-ttu-id="63693-134">System. String</span><span class="sxs-lookup"><span data-stu-id="63693-134">System.String</span></span>

## <span data-ttu-id="63693-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63693-135">OUTPUTS</span></span>

### <span data-ttu-id="63693-136">Microsoft. Azure. Commands. Sql. Backup. model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="63693-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="63693-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63693-137">NOTES</span></span>

## <span data-ttu-id="63693-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63693-138">RELATED LINKS</span></span>