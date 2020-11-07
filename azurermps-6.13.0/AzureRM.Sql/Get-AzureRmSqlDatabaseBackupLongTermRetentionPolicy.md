---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: dcc8d99cdf179ed3e069ef82fe758c4c699054a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762890"
---
# <span data-ttu-id="b7f2e-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b7f2e-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="b7f2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7f2e-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f2e-103">Bir veritabanı uzun bekletme ilkesi alır.</span><span class="sxs-lookup"><span data-stu-id="b7f2e-103">Gets a database long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7f2e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b7f2e-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-Current] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7f2e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b7f2e-105">DESCRIPTION</span></span>
<span data-ttu-id="b7f2e-106">**Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet 'i, bu veritabanına kaydedilen uzun süreli bekletme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="b7f2e-106">The **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="b7f2e-107">İlke, yedek depolama ilkesini tanımlamak için kullanılan bir Azure yedekleme kaynağı.</span><span class="sxs-lookup"><span data-stu-id="b7f2e-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="b7f2e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b7f2e-108">EXAMPLES</span></span>

### <span data-ttu-id="b7f2e-109">Örnek 1: uzun süreli bekletme ilkesinin geçerli sürümünü alma</span><span class="sxs-lookup"><span data-stu-id="b7f2e-109">Example 1: Get the current version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -Current


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

<span data-ttu-id="b7f2e-110">Bu komut, database01 için uzun süreli bekletme ilkesinin geçerli sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="b7f2e-110">This command gets the current version of the long term retention policy for database01</span></span>

### <span data-ttu-id="b7f2e-111">Örnek 2: uzun süreli bekletme ilkesinin eski sürümünü edinin</span><span class="sxs-lookup"><span data-stu-id="b7f2e-111">Example 2: Get the legacy version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        :
MonthlyRetention                       :
YearlyRetention                        :
WeekOfYear                             :
State                                  : Enabled
RecoveryServicesBackupPolicyResourceId : /subscriptions/4f2b42fc-4fc3-fd41-8ab8-5a382d8b30df/resourceGroups/resourcegroup01/providers/MicrosoftRecoveryServices/vaults/vault01/backupPolicies/policy01
Location                               : Southeast Asia
```

<span data-ttu-id="b7f2e-112">Bu komut, database01 için uzun süreli bekletme ilkesinin eski sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="b7f2e-112">This command gets the legacy version of the long term retention policy for database01</span></span>

## <span data-ttu-id="b7f2e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b7f2e-113">PARAMETERS</span></span>

### <span data-ttu-id="b7f2e-114">-Geçerli</span><span class="sxs-lookup"><span data-stu-id="b7f2e-114">-Current</span></span>
<span data-ttu-id="b7f2e-115">Sağlanmazsa, komut eski uzun süreli bekletme ilkesi bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b7f2e-115">If not provided, the command returns the legacy Long Term Retention policy information.</span></span>
<span data-ttu-id="b7f2e-116">Aksi takdirde komut, uzun süreli bekletme ilkesinin geçerli sürümünü döndürür.</span><span class="sxs-lookup"><span data-stu-id="b7f2e-116">Otherwise, the command returns the current version of the Long Term Retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7f2e-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b7f2e-117">-DatabaseName</span></span>
<span data-ttu-id="b7f2e-118">Kullanılacak Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="b7f2e-118">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="b7f2e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7f2e-119">-DefaultProfile</span></span>
<span data-ttu-id="b7f2e-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b7f2e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7f2e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7f2e-121">-ResourceGroupName</span></span>
<span data-ttu-id="b7f2e-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b7f2e-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="b7f2e-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b7f2e-123">-ServerName</span></span>
<span data-ttu-id="b7f2e-124">Veritabanının bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="b7f2e-124">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="b7f2e-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="b7f2e-125">-Confirm</span></span>
<span data-ttu-id="b7f2e-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b7f2e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7f2e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7f2e-127">-WhatIf</span></span>
<span data-ttu-id="b7f2e-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b7f2e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7f2e-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b7f2e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7f2e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f2e-130">CommonParameters</span></span>
<span data-ttu-id="b7f2e-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b7f2e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f2e-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7f2e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f2e-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b7f2e-133">INPUTS</span></span>

### <span data-ttu-id="b7f2e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b7f2e-134">System.String</span></span>

## <span data-ttu-id="b7f2e-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b7f2e-135">OUTPUTS</span></span>

### <span data-ttu-id="b7f2e-136">Microsoft. Azure. Commands. Sql. Backup. model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b7f2e-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="b7f2e-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b7f2e-137">NOTES</span></span>

## <span data-ttu-id="b7f2e-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b7f2e-138">RELATED LINKS</span></span>

[<span data-ttu-id="b7f2e-139">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b7f2e-139">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="b7f2e-140">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b7f2e-140">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="b7f2e-141">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b7f2e-141">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="b7f2e-142">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="b7f2e-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
