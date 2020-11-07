---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Get-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
ms.openlocfilehash: caab43824c63e73e7011c0377d0bd7665befe5dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591973"
---
# <span data-ttu-id="4fdd3-101">Get-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="4fdd3-101">Get-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="4fdd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fdd3-102">SYNOPSIS</span></span>
<span data-ttu-id="4fdd3-103">Bir Azure veritabanı geçiş hizmeti geçiş göreviyle ilişkili PSProjectTask nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="4fdd3-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fdd3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4fdd3-104">SYNTAX</span></span>

### <span data-ttu-id="4fdd3-105">ListByComponent (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4fdd3-105">ListByComponent (Default)</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fdd3-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="4fdd3-106">ListByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fdd3-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="4fdd3-107">GetByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fdd3-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="4fdd3-108">GetByInputObjectResultType</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fdd3-109">Listebyresourceıd</span><span class="sxs-lookup"><span data-stu-id="4fdd3-109">ListByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fdd3-110">Getbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="4fdd3-110">GetByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fdd3-111">Getbyresourceıdresulttype</span><span class="sxs-lookup"><span data-stu-id="4fdd3-111">GetByResourceIdResultType</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fdd3-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="4fdd3-112">GetByComponent</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fdd3-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="4fdd3-113">GetByComponentResultType</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4fdd3-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="4fdd3-114">DESCRIPTION</span></span>
<span data-ttu-id="4fdd3-115">Get-AzureRmDataMigrationTask cmdlet 'i, Azure veritabanı geçiş hizmeti geçiş göreviyle ilişkili özellikleri alır.</span><span class="sxs-lookup"><span data-stu-id="4fdd3-115">The Get-AzureRmDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="4fdd3-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4fdd3-116">EXAMPLES</span></span>

### <span data-ttu-id="4fdd3-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4fdd3-117">Example 1</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="4fdd3-118">Yukarıdaki örnek, giriş parametresi olarak geçirilen görev adına dayalı bir Azure veritabanı geçiş hizmeti geçiş göreviyle ilişkili özellikleri almak için Get-AzureRmDataMigrationTask cmdlet kullanımını gösterir</span><span class="sxs-lookup"><span data-stu-id="4fdd3-118">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="4fdd3-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4fdd3-119">Example 2</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -Project $myProject
```

<span data-ttu-id="4fdd3-120">Yukarıdaki örnek, giriş parametresi olarak geçirilen PSProject nesnesiyle ilişkili geçiş görevlerinin tümünü almak için Get-AzureRmDataMigrationTask cmdlet kullanımını gösterir</span><span class="sxs-lookup"><span data-stu-id="4fdd3-120">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="4fdd3-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4fdd3-121">PARAMETERS</span></span>

### <span data-ttu-id="4fdd3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fdd3-122">-DefaultProfile</span></span>
<span data-ttu-id="4fdd3-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4fdd3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fdd3-124">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="4fdd3-124">-Expand</span></span>
<span data-ttu-id="4fdd3-125">Çıktıyı genişletme</span><span class="sxs-lookup"><span data-stu-id="4fdd3-125">Expand output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObject, GetByResourceId, GetByComponent
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fdd3-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fdd3-126">-InputObject</span></span>
<span data-ttu-id="4fdd3-127">PSProject nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4fdd3-127">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ListByInputObject
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: GetByInputObject, GetByInputObjectResultType
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fdd3-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="4fdd3-128">-Name</span></span>
<span data-ttu-id="4fdd3-129">Görevin adı.</span><span class="sxs-lookup"><span data-stu-id="4fdd3-129">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByInputObject, GetByInputObjectResultType, GetByResourceId, GetByResourceIdResultType, GetByComponentResultType
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByComponent
Aliases: TaskName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fdd3-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="4fdd3-130">-ProjectName</span></span>
<span data-ttu-id="4fdd3-131">Projenin adı.</span><span class="sxs-lookup"><span data-stu-id="4fdd3-131">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fdd3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fdd3-132">-ResourceGroupName</span></span>
<span data-ttu-id="4fdd3-133">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4fdd3-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fdd3-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4fdd3-134">-ResourceId</span></span>
<span data-ttu-id="4fdd3-135">Proje kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="4fdd3-135">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceId, GetByResourceIdResultType
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fdd3-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="4fdd3-136">-ResultType</span></span>
<span data-ttu-id="4fdd3-137">Verilen sonuç türünün çıkışını genişletme.</span><span class="sxs-lookup"><span data-stu-id="4fdd3-137">Expand output of given result type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput, LoginLevelOutput, AgentJobLevelOutput

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fdd3-138">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="4fdd3-138">-ServiceName</span></span>
<span data-ttu-id="4fdd3-139">Veritabanı geçiş hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="4fdd3-139">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fdd3-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="4fdd3-140">-TaskType</span></span>
<span data-ttu-id="4fdd3-141">Göreve göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="4fdd3-141">Filter by TaskType.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum]
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fdd3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fdd3-142">CommonParameters</span></span>
<span data-ttu-id="4fdd3-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4fdd3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fdd3-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fdd3-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fdd3-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4fdd3-145">INPUTS</span></span>

### <span data-ttu-id="4fdd3-146">Microsoft. Azure. Commands. DataMigration. modeller. PSProject</span><span class="sxs-lookup"><span data-stu-id="4fdd3-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="4fdd3-147">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4fdd3-147">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="4fdd3-148">System. String</span><span class="sxs-lookup"><span data-stu-id="4fdd3-148">System.String</span></span>

## <span data-ttu-id="4fdd3-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4fdd3-149">OUTPUTS</span></span>

### <span data-ttu-id="4fdd3-150">Microsoft. Azure. Commands. DataMigration. modeller. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="4fdd3-150">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="4fdd3-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4fdd3-151">NOTES</span></span>

## <span data-ttu-id="4fdd3-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4fdd3-152">RELATED LINKS</span></span>