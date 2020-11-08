---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Stop-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 2a7c74c4c8fef61e01ccbbb512ff428b9e885f06
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266769"
---
# <span data-ttu-id="e8a5e-101">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="e8a5e-101">Stop-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="e8a5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8a5e-102">SYNOPSIS</span></span>
<span data-ttu-id="e8a5e-103">Veritabanını bırakarak günlük yürütme hizmetini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="e8a5e-103">Cancels the Log Replay service by dropping the database.</span></span>

## <span data-ttu-id="e8a5e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8a5e-104">SYNTAX</span></span>

### <span data-ttu-id="e8a5e-105">Logreplayınstancedatabasefrominınputparameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e8a5e-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8a5e-106">Logreplayınstancedatabasefrolauressqlmanageddatabasemodelınstancedefinition</span><span class="sxs-lookup"><span data-stu-id="e8a5e-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-PassThru] [-InputObject] <AzureSqlManagedDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8a5e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8a5e-107">DESCRIPTION</span></span>
<span data-ttu-id="e8a5e-108">**Stop-Azsqlınstancedatabaselogreplay** cmdlet 'i veritabanını bırakır ve ardından log Replay hizmetini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="e8a5e-108">The **Stop-AzSqlInstanceDatabaseLogReplay** cmdlet drops the database and thus cancel Log Replay service.</span></span>

## <span data-ttu-id="e8a5e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8a5e-109">EXAMPLES</span></span>

### <span data-ttu-id="e8a5e-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e8a5e-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="e8a5e-111">Bu komut, verilen veritabanında günlük yürütme hizmetini iptal edecektir.</span><span class="sxs-lookup"><span data-stu-id="e8a5e-111">This command will cancel log replay service on the given database.</span></span>

## <span data-ttu-id="e8a5e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8a5e-112">PARAMETERS</span></span>

### <span data-ttu-id="e8a5e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8a5e-113">-DefaultProfile</span></span>
<span data-ttu-id="e8a5e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8a5e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8a5e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e8a5e-115">-Force</span></span>
<span data-ttu-id="e8a5e-116">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="e8a5e-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="e8a5e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8a5e-117">-InputObject</span></span>
<span data-ttu-id="e8a5e-118">Örnek veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e8a5e-118">The instance database object.</span></span>

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

### <span data-ttu-id="e8a5e-119">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e8a5e-119">-InstanceName</span></span>
<span data-ttu-id="e8a5e-120">Örneğin adı.</span><span class="sxs-lookup"><span data-stu-id="e8a5e-120">The name of the instance.</span></span>

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

### <span data-ttu-id="e8a5e-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="e8a5e-121">-Name</span></span>
<span data-ttu-id="e8a5e-122">Örnek veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="e8a5e-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="e8a5e-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e8a5e-123">-PassThru</span></span>
<span data-ttu-id="e8a5e-124">Eşitleme grubunu iade edilip edilmeyeceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="e8a5e-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="e8a5e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8a5e-125">-ResourceGroupName</span></span>
<span data-ttu-id="e8a5e-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e8a5e-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="e8a5e-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="e8a5e-127">-Confirm</span></span>
<span data-ttu-id="e8a5e-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e8a5e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8a5e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8a5e-129">-WhatIf</span></span>
<span data-ttu-id="e8a5e-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8a5e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8a5e-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e8a5e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8a5e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8a5e-132">CommonParameters</span></span>
<span data-ttu-id="e8a5e-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8a5e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8a5e-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e8a5e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8a5e-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8a5e-135">INPUTS</span></span>

### <span data-ttu-id="e8a5e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e8a5e-136">System.String</span></span>

### <span data-ttu-id="e8a5e-137">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="e8a5e-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="e8a5e-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8a5e-138">OUTPUTS</span></span>

### <span data-ttu-id="e8a5e-139">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="e8a5e-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="e8a5e-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8a5e-140">NOTES</span></span>

## <span data-ttu-id="e8a5e-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8a5e-141">RELATED LINKS</span></span>
