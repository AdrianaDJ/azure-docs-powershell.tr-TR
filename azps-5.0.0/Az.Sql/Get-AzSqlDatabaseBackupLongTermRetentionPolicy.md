---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0dd5f38f00e715141a967160cadc8ab075825ac6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276692"
---
# <span data-ttu-id="3793d-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3793d-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="3793d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3793d-102">SYNOPSIS</span></span>
<span data-ttu-id="3793d-103">Bir veritabanı uzun bekletme ilkesi alır.</span><span class="sxs-lookup"><span data-stu-id="3793d-103">Gets a database long term retention policy.</span></span>

## <span data-ttu-id="3793d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3793d-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3793d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3793d-105">DESCRIPTION</span></span>
<span data-ttu-id="3793d-106">**Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet 'i, bu veritabanına kaydedilen uzun süreli bekletme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="3793d-106">The **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="3793d-107">İlke, yedek depolama ilkesini tanımlamak için kullanılan bir Azure yedekleme kaynağı.</span><span class="sxs-lookup"><span data-stu-id="3793d-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="3793d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3793d-108">EXAMPLES</span></span>

### <span data-ttu-id="3793d-109">Örnek 1: uzun süreli bekletme ilkesinin geçerli sürümünü alma</span><span class="sxs-lookup"><span data-stu-id="3793d-109">Example 1: Get the current version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="3793d-110">Bu komut, database01 için uzun süreli bekletme ilkesinin geçerli sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="3793d-110">This command gets the current version of the long term retention policy for database01</span></span>

## <span data-ttu-id="3793d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3793d-111">PARAMETERS</span></span>

### <span data-ttu-id="3793d-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3793d-112">-DatabaseName</span></span>
<span data-ttu-id="3793d-113">Kullanılacak Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="3793d-113">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="3793d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3793d-114">-DefaultProfile</span></span>
<span data-ttu-id="3793d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3793d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3793d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3793d-116">-ResourceGroupName</span></span>
<span data-ttu-id="3793d-117">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3793d-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="3793d-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3793d-118">-ServerName</span></span>
<span data-ttu-id="3793d-119">Veritabanının bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="3793d-119">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="3793d-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="3793d-120">-Confirm</span></span>
<span data-ttu-id="3793d-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3793d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3793d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3793d-122">-WhatIf</span></span>
<span data-ttu-id="3793d-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3793d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3793d-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3793d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3793d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3793d-125">CommonParameters</span></span>
<span data-ttu-id="3793d-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3793d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3793d-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3793d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3793d-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3793d-128">INPUTS</span></span>

### <span data-ttu-id="3793d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3793d-129">System.String</span></span>

## <span data-ttu-id="3793d-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3793d-130">OUTPUTS</span></span>

### <span data-ttu-id="3793d-131">Microsoft. Azure. Commands. Sql. Backup. model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="3793d-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="3793d-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3793d-132">NOTES</span></span>

## <span data-ttu-id="3793d-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3793d-133">RELATED LINKS</span></span>

[<span data-ttu-id="3793d-134">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="3793d-134">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="3793d-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="3793d-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="3793d-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3793d-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="3793d-137">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="3793d-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)