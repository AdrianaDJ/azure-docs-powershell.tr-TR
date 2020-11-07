---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
ms.openlocfilehash: c40bd5761d7e0966e7d756a758f79bfb3592a2ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761027"
---
# <span data-ttu-id="dcdb3-101">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="dcdb3-101">New-AzDataMigrationTask</span></span>

## <span data-ttu-id="dcdb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcdb3-102">SYNOPSIS</span></span>
<span data-ttu-id="dcdb3-103">Azure veritabanı geçiş hizmeti 'nde veri geçişi görevini oluşturur ve başlatır.</span><span class="sxs-lookup"><span data-stu-id="dcdb3-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

## <span data-ttu-id="dcdb3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dcdb3-104">SYNTAX</span></span>

### <span data-ttu-id="dcdb3-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dcdb3-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dcdb3-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="dcdb3-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcdb3-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="dcdb3-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcdb3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="dcdb3-108">DESCRIPTION</span></span>
<span data-ttu-id="dcdb3-109">New-AzDataMigrationTask cmdlet 'i veri geçişi görevini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dcdb3-109">The New-AzDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="dcdb3-110">Bu cmdlet, görev türü Numaralandırıcı, Azure Kaynak grubu, ilişkili Azure veritabanı geçiş hizmeti ve Project 'in adını giriş olarak alır.</span><span class="sxs-lookup"><span data-stu-id="dcdb3-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="dcdb3-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dcdb3-111">EXAMPLES</span></span>

### <span data-ttu-id="dcdb3-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dcdb3-112">Example 1</span></span>
```
PS C:\> New-AzDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs -MigrationValidation $validationTask
```

<span data-ttu-id="dcdb3-113">Bu örnek komut dosyası, Myvseçmsproject adlı projede MyMigrationTask adlı yeni bir veri taşıma görevinin ve TestService adlı hizmetin nasıl oluşturulduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="dcdb3-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="dcdb3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dcdb3-114">PARAMETERS</span></span>

### <span data-ttu-id="dcdb3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcdb3-115">-DefaultProfile</span></span>
<span data-ttu-id="dcdb3-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dcdb3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcdb3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dcdb3-117">-InputObject</span></span>
<span data-ttu-id="dcdb3-118">PSProject nesnesi.</span><span class="sxs-lookup"><span data-stu-id="dcdb3-118">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcdb3-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="dcdb3-119">-Name</span></span>
<span data-ttu-id="dcdb3-120">Görevin adı.</span><span class="sxs-lookup"><span data-stu-id="dcdb3-120">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcdb3-121">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="dcdb3-121">-ProjectName</span></span>
<span data-ttu-id="dcdb3-122">Projenin adı.</span><span class="sxs-lookup"><span data-stu-id="dcdb3-122">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcdb3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcdb3-123">-ResourceGroupName</span></span>
<span data-ttu-id="dcdb3-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="dcdb3-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcdb3-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="dcdb3-125">-ResourceId</span></span>
<span data-ttu-id="dcdb3-126">Proje kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="dcdb3-126">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcdb3-127">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="dcdb3-127">-ServiceName</span></span>
<span data-ttu-id="dcdb3-128">Veritabanı geçiş hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="dcdb3-128">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcdb3-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="dcdb3-129">-TaskType</span></span>
<span data-ttu-id="dcdb3-130">Görev türü.</span><span class="sxs-lookup"><span data-stu-id="dcdb3-130">Task Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync, ConnectToSourceMongoDb, ConnectToTargetMongoDb, MigrateMongoDb, ValidateMongoDbMigration, ConnectToTargetSqlDbMiSync, ValidateSqlServerSqlDbMiSync, MigrateSqlServerSqlDbMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcdb3-131">-MigrationValidation</span><span class="sxs-lookup"><span data-stu-id="dcdb3-131">-MigrationValidation</span></span> 
<span data-ttu-id="dcdb3-132">Doğrulama çağrısıyla görev yanıtı nesnesi isteğe bağlıdır ancak önerilir.</span><span class="sxs-lookup"><span data-stu-id="dcdb3-132">Task response object by validation call, optional but recommended.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcdb3-133">-Bekleme</span><span class="sxs-lookup"><span data-stu-id="dcdb3-133">-Wait</span></span>
<span data-ttu-id="dcdb3-134">Görevin bitmesini bekleme.</span><span class="sxs-lookup"><span data-stu-id="dcdb3-134">Whether to wait for task to finish.</span></span> <span data-ttu-id="dcdb3-135">Bayrak ayarlanırsa, göreve kadar her bir saniye kadar denetler ve çıkış veya hatanın denetlendiği görev özelliklerini kullanıcıya döndürür.</span><span class="sxs-lookup"><span data-stu-id="dcdb3-135">If the flag is set, checks every one seconds till the task finishes and return to user the task properties where output or error can be inspected.</span></span> 
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

### <span data-ttu-id="dcdb3-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="dcdb3-136">-Confirm</span></span>
<span data-ttu-id="dcdb3-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dcdb3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcdb3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcdb3-138">-WhatIf</span></span>
<span data-ttu-id="dcdb3-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dcdb3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcdb3-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dcdb3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcdb3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcdb3-141">CommonParameters</span></span>
<span data-ttu-id="dcdb3-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dcdb3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcdb3-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcdb3-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcdb3-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dcdb3-144">INPUTS</span></span>

### <span data-ttu-id="dcdb3-145">Microsoft. Azure. Commands. DataMigration. modeller. PSProject</span><span class="sxs-lookup"><span data-stu-id="dcdb3-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="dcdb3-146">System. String</span><span class="sxs-lookup"><span data-stu-id="dcdb3-146">System.String</span></span>

## <span data-ttu-id="dcdb3-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dcdb3-147">OUTPUTS</span></span>

### <span data-ttu-id="dcdb3-148">Microsoft. Azure. Commands. DataMigration. modeller. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="dcdb3-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="dcdb3-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dcdb3-149">NOTES</span></span>

## <span data-ttu-id="dcdb3-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dcdb3-150">RELATED LINKS</span></span>
