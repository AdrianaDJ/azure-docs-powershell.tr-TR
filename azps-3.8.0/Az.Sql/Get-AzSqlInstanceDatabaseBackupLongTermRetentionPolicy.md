---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 5fe99e867f4646edc55b2ab304f6549628955a03
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104288"
---
# <span data-ttu-id="c9b39-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c9b39-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="c9b39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9b39-102">SYNOPSIS</span></span>
<span data-ttu-id="c9b39-103">Yönetilen veritabanının uzun süreli bekletme ilkesini alır</span><span class="sxs-lookup"><span data-stu-id="c9b39-103">Gets a managed database's long term retention policy</span></span>

## <span data-ttu-id="c9b39-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9b39-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9b39-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9b39-105">DESCRIPTION</span></span>
<span data-ttu-id="c9b39-106">**Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet 'i, bu yönetilen veritabanına kaydedilen uzun süreli bekletme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="c9b39-106">The **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this managed database.</span></span>
<span data-ttu-id="c9b39-107">İlke, yedek depolama ilkesini tanımlamak için kullanılan bir Azure yedekleme kaynağı.</span><span class="sxs-lookup"><span data-stu-id="c9b39-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="c9b39-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9b39-108">EXAMPLES</span></span>

### <span data-ttu-id="c9b39-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c9b39-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : test
WeeklyRetention     : P2W
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="c9b39-110">Veritabanı için uzun süreli bekletme ilkesinin geçerli sürümünü alır</span><span class="sxs-lookup"><span data-stu-id="c9b39-110">Gets the current version of the long term retention policy for the database</span></span>

## <span data-ttu-id="c9b39-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9b39-111">PARAMETERS</span></span>

### <span data-ttu-id="c9b39-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c9b39-112">-DatabaseName</span></span>
<span data-ttu-id="c9b39-113">Kullanılacak Azure yönetilen veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="c9b39-113">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="c9b39-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9b39-114">-DefaultProfile</span></span>
<span data-ttu-id="c9b39-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c9b39-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b39-116">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c9b39-116">-InstanceName</span></span>
<span data-ttu-id="c9b39-117">Veritabanının ait olduğu Azure yönetilen örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="c9b39-117">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="c9b39-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9b39-118">-ResourceGroupName</span></span>
<span data-ttu-id="c9b39-119">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c9b39-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="c9b39-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="c9b39-120">-Confirm</span></span>
<span data-ttu-id="c9b39-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c9b39-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b39-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9b39-122">-WhatIf</span></span>
<span data-ttu-id="c9b39-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9b39-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9b39-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c9b39-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b39-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9b39-125">CommonParameters</span></span>
<span data-ttu-id="c9b39-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9b39-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9b39-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c9b39-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9b39-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9b39-128">INPUTS</span></span>

### <span data-ttu-id="c9b39-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c9b39-129">System.String</span></span>

## <span data-ttu-id="c9b39-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9b39-130">OUTPUTS</span></span>

### <span data-ttu-id="c9b39-131">Microsoft. Azure. Commands. Sql. ManagedDatabaseBackup. model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c9b39-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="c9b39-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9b39-132">NOTES</span></span>

## <span data-ttu-id="c9b39-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9b39-133">RELATED LINKS</span></span>

[<span data-ttu-id="c9b39-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="c9b39-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="c9b39-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="c9b39-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="c9b39-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c9b39-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="c9b39-137">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="c9b39-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)