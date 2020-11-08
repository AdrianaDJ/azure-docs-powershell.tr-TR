---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Complete-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: d1d7cead951520944199347ebdbb209c5474eb3e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268755"
---
# <span data-ttu-id="341e9-101">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="341e9-101">Complete-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="341e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="341e9-102">SYNOPSIS</span></span>
<span data-ttu-id="341e9-103">Verilen veritabanı için günlük yeniden yürütme hizmetini tamamlar.</span><span class="sxs-lookup"><span data-stu-id="341e9-103">Completes Log Replay service for the given database.</span></span>

## <span data-ttu-id="341e9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="341e9-104">SYNTAX</span></span>

### <span data-ttu-id="341e9-105">Logreplayınstancedatabasefrominınputparameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="341e9-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="341e9-106">Logreplayınstancedatabasefrolauressqlmanageddatabasemodelınstancedefinition</span><span class="sxs-lookup"><span data-stu-id="341e9-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="341e9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="341e9-107">DESCRIPTION</span></span>
<span data-ttu-id="341e9-108">**Tam-Azsqlınstancedatabaselogreplay** cmdlet 'i, verilen veritabanında günlük yürütme hizmetini tamamlar.</span><span class="sxs-lookup"><span data-stu-id="341e9-108">The **Complete-AzSqlInstanceDatabaseLogReplay** cmdlet completes the Log Replay service on the given database.</span></span>

## <span data-ttu-id="341e9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="341e9-109">EXAMPLES</span></span>

### <span data-ttu-id="341e9-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="341e9-110">Example 1</span></span>
```powershell
PS C:\> Complete-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName" -LastBackupName "last_backup.bak"
```

<span data-ttu-id="341e9-111">Bu komut, son yedekleme geri yüklendikten sonra verilen veritabanı için günlük yeniden yürütme hizmetini tamamlar.</span><span class="sxs-lookup"><span data-stu-id="341e9-111">This command will complete Log Replay service for the given database after last backup gets restored.</span></span>

## <span data-ttu-id="341e9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="341e9-112">PARAMETERS</span></span>

### <span data-ttu-id="341e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="341e9-113">-DefaultProfile</span></span>
<span data-ttu-id="341e9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="341e9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="341e9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="341e9-115">-InputObject</span></span>
<span data-ttu-id="341e9-116">Örnek veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="341e9-116">The instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="341e9-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="341e9-117">-InstanceName</span></span>
<span data-ttu-id="341e9-118">Örneğin adı.</span><span class="sxs-lookup"><span data-stu-id="341e9-118">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="341e9-119">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="341e9-119">-LastBackupName</span></span>
<span data-ttu-id="341e9-120">Geri yüklenecek son yedekleme dosyasının adı.</span><span class="sxs-lookup"><span data-stu-id="341e9-120">The name of the last backup file to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="341e9-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="341e9-121">-Name</span></span>
<span data-ttu-id="341e9-122">Örnek veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="341e9-122">The name of the instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="341e9-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="341e9-123">-PassThru</span></span>
<span data-ttu-id="341e9-124">Eşitleme grubunu iade edilip edilmeyeceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="341e9-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="341e9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="341e9-125">-ResourceGroupName</span></span>
<span data-ttu-id="341e9-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="341e9-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="341e9-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="341e9-127">-Confirm</span></span>
<span data-ttu-id="341e9-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="341e9-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="341e9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="341e9-129">-WhatIf</span></span>
<span data-ttu-id="341e9-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="341e9-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="341e9-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="341e9-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="341e9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="341e9-132">CommonParameters</span></span>
<span data-ttu-id="341e9-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="341e9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="341e9-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="341e9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="341e9-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="341e9-135">INPUTS</span></span>

### <span data-ttu-id="341e9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="341e9-136">System.String</span></span>

### <span data-ttu-id="341e9-137">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="341e9-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="341e9-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="341e9-138">OUTPUTS</span></span>

## <span data-ttu-id="341e9-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="341e9-139">NOTES</span></span>

## <span data-ttu-id="341e9-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="341e9-140">RELATED LINKS</span></span>
