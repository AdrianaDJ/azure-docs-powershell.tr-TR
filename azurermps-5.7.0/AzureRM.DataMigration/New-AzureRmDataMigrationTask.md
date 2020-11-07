---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
ms.openlocfilehash: 1bdf66311acd1b8ff1de43b5ea199d5d0a17c394
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762649"
---
# <span data-ttu-id="d83ea-101">New-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="d83ea-101">New-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="d83ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d83ea-102">SYNOPSIS</span></span>
<span data-ttu-id="d83ea-103">Azure veritabanı geçiş hizmeti 'nde veri geçişi görevini oluşturur ve başlatır.</span><span class="sxs-lookup"><span data-stu-id="d83ea-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d83ea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d83ea-104">SYNTAX</span></span>

### <span data-ttu-id="d83ea-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d83ea-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d83ea-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="d83ea-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d83ea-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d83ea-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="d83ea-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d83ea-108">DESCRIPTION</span></span>
<span data-ttu-id="d83ea-109">New-AzureRmDataMigrationTask cmdlet 'i veri geçişi görevini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d83ea-109">The New-AzureRmDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="d83ea-110">Bu cmdlet, görev türü Numaralandırıcı, Azure Kaynak grubu, ilişkili Azure veri taşıma hizmeti ve Project 'in adını giriş olarak alır.</span><span class="sxs-lookup"><span data-stu-id="d83ea-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Data Migration Service and Project as input.</span></span> 

## <span data-ttu-id="d83ea-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d83ea-111">EXAMPLES</span></span>

### <span data-ttu-id="d83ea-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d83ea-112">Example 1</span></span>
```
PS C:\> New-AzureRmDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs
```
<span data-ttu-id="d83ea-113">Bu örnek komut dosyası, Myvseçmsproject adlı projede MyMigrationTask adlı yeni bir veri taşıma görevinin ve TestService adlı hizmetin nasıl oluşturulduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="d83ea-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="d83ea-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d83ea-114">PARAMETERS</span></span>

### <span data-ttu-id="d83ea-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="d83ea-115">-Confirm</span></span>
<span data-ttu-id="d83ea-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d83ea-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d83ea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d83ea-117">-DefaultProfile</span></span>
<span data-ttu-id="d83ea-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d83ea-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d83ea-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d83ea-119">-InputObject</span></span>
<span data-ttu-id="d83ea-120">PSProject nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d83ea-120">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d83ea-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="d83ea-121">-Name</span></span>
<span data-ttu-id="d83ea-122">Görevin adı.</span><span class="sxs-lookup"><span data-stu-id="d83ea-122">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d83ea-123">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="d83ea-123">-ProjectName</span></span>
<span data-ttu-id="d83ea-124">Projenin adı.</span><span class="sxs-lookup"><span data-stu-id="d83ea-124">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d83ea-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d83ea-125">-ResourceGroupName</span></span>
<span data-ttu-id="d83ea-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d83ea-126">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d83ea-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d83ea-127">-ResourceId</span></span>
<span data-ttu-id="d83ea-128">Proje kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="d83ea-128">Project Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d83ea-129">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="d83ea-129">-ServiceName</span></span>
<span data-ttu-id="d83ea-130">Veri geçişi hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="d83ea-130">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d83ea-131">-TaskType</span><span class="sxs-lookup"><span data-stu-id="d83ea-131">-TaskType</span></span>
<span data-ttu-id="d83ea-132">Görev türü.</span><span class="sxs-lookup"><span data-stu-id="d83ea-132">Task Type.</span></span>

```yaml
Type: TaskTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d83ea-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d83ea-133">-WhatIf</span></span>
<span data-ttu-id="d83ea-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d83ea-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d83ea-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d83ea-135">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="d83ea-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d83ea-136">INPUTS</span></span>

### <span data-ttu-id="d83ea-137">Microsoft. Azure. Commands. DataMigration. modeller. PSProject</span><span class="sxs-lookup"><span data-stu-id="d83ea-137">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="d83ea-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d83ea-138">System.String</span></span>


## <span data-ttu-id="d83ea-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d83ea-139">OUTPUTS</span></span>

### <span data-ttu-id="d83ea-140">Microsoft. Azure. Commands. DataMigration. modeller. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="d83ea-140">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>


## <span data-ttu-id="d83ea-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d83ea-141">NOTES</span></span>

## <span data-ttu-id="d83ea-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d83ea-142">RELATED LINKS</span></span>


