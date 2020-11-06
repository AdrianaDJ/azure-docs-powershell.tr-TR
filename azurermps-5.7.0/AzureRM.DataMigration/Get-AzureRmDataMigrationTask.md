---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
ms.openlocfilehash: 5ca6edfa811a1b73cbdaae59e8d3b0e2f76cc15f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589810"
---
# <span data-ttu-id="54363-101">Get-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="54363-101">Get-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="54363-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54363-102">SYNOPSIS</span></span>
<span data-ttu-id="54363-103">Bir Azure veritabanı geçiş hizmeti geçiş göreviyle ilişkili PSProjectTask nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="54363-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54363-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54363-104">SYNTAX</span></span>

### <span data-ttu-id="54363-105">ListByComponent (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="54363-105">ListByComponent (Default)</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="54363-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="54363-106">ListByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="54363-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="54363-107">GetByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="54363-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="54363-108">GetByInputObjectResultType</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="54363-109">Listebyresourceıd</span><span class="sxs-lookup"><span data-stu-id="54363-109">ListByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="54363-110">Getbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="54363-110">GetByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="54363-111">Getbyresourceıdresulttype</span><span class="sxs-lookup"><span data-stu-id="54363-111">GetByResourceIdResultType</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="54363-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="54363-112">GetByComponent</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="54363-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="54363-113">GetByComponentResultType</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="54363-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="54363-114">DESCRIPTION</span></span>
<span data-ttu-id="54363-115">Get-AzureRmDataMigrationTask cmdlet 'i, Azure veritabanı geçiş hizmeti geçiş göreviyle ilişkili özellikleri alır.</span><span class="sxs-lookup"><span data-stu-id="54363-115">The Get-AzureRmDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="54363-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54363-116">EXAMPLES</span></span>

### <span data-ttu-id="54363-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="54363-117">Example 1</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="54363-118">Yukarıdaki örnek, giriş parametresi olarak geçirilen görev adına dayalı bir Azure veritabanı geçiş hizmeti geçiş göreviyle ilişkili özellikleri almak için Get-AzureRmDataMigrationTask cmdlet kullanımını gösterir</span><span class="sxs-lookup"><span data-stu-id="54363-118">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="54363-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="54363-119">Example 2</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -Project $myProject
```

<span data-ttu-id="54363-120">Yukarıdaki örnek, giriş parametresi olarak geçirilen PSProject nesnesiyle ilişkili geçiş görevlerinin tümünü almak için Get-AzureRmDataMigrationTask cmdlet kullanımını gösterir</span><span class="sxs-lookup"><span data-stu-id="54363-120">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="54363-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54363-121">PARAMETERS</span></span>

### <span data-ttu-id="54363-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54363-122">-DefaultProfile</span></span>
<span data-ttu-id="54363-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="54363-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54363-124">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="54363-124">-Expand</span></span>
<span data-ttu-id="54363-125">Çıktıyı genişletme</span><span class="sxs-lookup"><span data-stu-id="54363-125">Expand output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetByInputObject, GetByResourceId, GetByComponent
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: SwitchParameter
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54363-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54363-126">-InputObject</span></span>
<span data-ttu-id="54363-127">PSProject nesnesi.</span><span class="sxs-lookup"><span data-stu-id="54363-127">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ListByInputObject
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSProject
Parameter Sets: GetByInputObject, GetByInputObjectResultType
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54363-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="54363-128">-Name</span></span>
<span data-ttu-id="54363-129">Görevin adı.</span><span class="sxs-lookup"><span data-stu-id="54363-129">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: GetByInputObject, GetByInputObjectResultType, GetByResourceId, GetByResourceIdResultType, GetByComponentResultType
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByComponent
Aliases: TaskName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54363-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="54363-130">-ProjectName</span></span>
<span data-ttu-id="54363-131">Projenin adı.</span><span class="sxs-lookup"><span data-stu-id="54363-131">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54363-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54363-132">-ResourceGroupName</span></span>
<span data-ttu-id="54363-133">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="54363-133">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54363-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="54363-134">-ResourceId</span></span>
<span data-ttu-id="54363-135">Proje kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="54363-135">Project Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceId, GetByResourceIdResultType
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54363-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="54363-136">-ResultType</span></span>
<span data-ttu-id="54363-137">Verilen sonuç türünün çıkışını genişletme.</span><span class="sxs-lookup"><span data-stu-id="54363-137">Expand output of given result type.</span></span>

```yaml
Type: ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases: 
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54363-138">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="54363-138">-ServiceName</span></span>
<span data-ttu-id="54363-139">Veri geçişi hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="54363-139">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54363-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="54363-140">-TaskType</span></span>
<span data-ttu-id="54363-141">Göreve göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="54363-141">Filter by TaskType.</span></span>

```yaml
Type: TaskTypeEnum
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases: 
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="54363-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54363-142">INPUTS</span></span>

### <span data-ttu-id="54363-143">Microsoft. Azure. Commands. DataMigration. modeller. PSProject</span><span class="sxs-lookup"><span data-stu-id="54363-143">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="54363-144">System. String</span><span class="sxs-lookup"><span data-stu-id="54363-144">System.String</span></span>

## <span data-ttu-id="54363-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54363-145">OUTPUTS</span></span>

### <span data-ttu-id="54363-146">System. Koleksiyonlar. Generic. IList ' 1 [[Microsoft. Azure. Commands. DataMigration. modeller. PSProjectTask, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="54363-146">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="54363-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54363-147">NOTES</span></span>

## <span data-ttu-id="54363-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54363-148">RELATED LINKS</span></span>

