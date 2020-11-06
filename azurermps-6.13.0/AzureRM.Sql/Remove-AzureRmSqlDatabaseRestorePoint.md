---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: be4a4f418268d1e2523e13d5a779f911381c7309
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591865"
---
# <span data-ttu-id="d49cb-101">Remove-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="d49cb-101">Remove-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="d49cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d49cb-102">SYNOPSIS</span></span>
<span data-ttu-id="d49cb-103">Bir SQL veritabanından geri yükleme noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d49cb-103">Removes given restore point from a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d49cb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d49cb-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d49cb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d49cb-105">DESCRIPTION</span></span>
<span data-ttu-id="d49cb-106">**Remove-AzureRmSqlDatabaseRestorePoint** cmdlet 'ı Azure SQL veritabanından geri yükleme noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d49cb-106">The **Remove-AzureRmSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>
<span data-ttu-id="d49cb-107">Bu cmdlet Şu anda Azure SQL veritabanında SQL Server DataWarehouse hizmeti tarafından desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="d49cb-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="d49cb-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d49cb-108">EXAMPLES</span></span>

### <span data-ttu-id="d49cb-109">Örnek 1: geri yükleme noktasını kaldırır</span><span class="sxs-lookup"><span data-stu-id="d49cb-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="d49cb-110">Bu komut, Azure SQL veritabanı 'nın oluşturma tarihi için geri yükleme noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d49cb-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="d49cb-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d49cb-111">PARAMETERS</span></span>

### <span data-ttu-id="d49cb-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d49cb-112">-DatabaseName</span></span>
<span data-ttu-id="d49cb-113">SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d49cb-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="d49cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d49cb-114">-DefaultProfile</span></span>
<span data-ttu-id="d49cb-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d49cb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d49cb-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d49cb-116">-PassThru</span></span>
<span data-ttu-id="d49cb-117">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="d49cb-117">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d49cb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d49cb-118">-ResourceGroupName</span></span>
<span data-ttu-id="d49cb-119">SQL veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d49cb-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="d49cb-120">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="d49cb-120">-RestorePointCreationDate</span></span>
<span data-ttu-id="d49cb-121">Geri yükleme noktası oluşturma tarihini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d49cb-121">Specifies the restore point creation date.</span></span>

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

### <span data-ttu-id="d49cb-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d49cb-122">-ServerName</span></span>
<span data-ttu-id="d49cb-123">Veritabanını barındıran AzureSQL sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d49cb-123">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="d49cb-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="d49cb-124">-Confirm</span></span>
<span data-ttu-id="d49cb-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d49cb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d49cb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d49cb-126">-WhatIf</span></span>
<span data-ttu-id="d49cb-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d49cb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d49cb-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d49cb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d49cb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d49cb-129">CommonParameters</span></span>
<span data-ttu-id="d49cb-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d49cb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d49cb-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d49cb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d49cb-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d49cb-132">INPUTS</span></span>

### <span data-ttu-id="d49cb-133">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="d49cb-133">System.DateTime</span></span>

### <span data-ttu-id="d49cb-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d49cb-134">System.String</span></span>

## <span data-ttu-id="d49cb-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d49cb-135">OUTPUTS</span></span>

### <span data-ttu-id="d49cb-136">Microsoft. Azure. Commands. Sql. Backup. model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="d49cb-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="d49cb-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d49cb-137">NOTES</span></span>

## <span data-ttu-id="d49cb-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d49cb-138">RELATED LINKS</span></span>
