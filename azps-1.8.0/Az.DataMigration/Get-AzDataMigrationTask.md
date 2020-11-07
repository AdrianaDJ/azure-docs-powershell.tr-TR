---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
ms.openlocfilehash: 65330f1024820c725cfb9a6b142000866063dc37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761040"
---
# <span data-ttu-id="af2b1-101">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="af2b1-101">Get-AzDataMigrationTask</span></span>

## <span data-ttu-id="af2b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af2b1-102">SYNOPSIS</span></span>
<span data-ttu-id="af2b1-103">Bir Azure veritabanı geçiş hizmeti geçiş göreviyle ilişkili PSProjectTask nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="af2b1-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="af2b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af2b1-104">SYNTAX</span></span>

### <span data-ttu-id="af2b1-105">ListByComponent (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="af2b1-105">ListByComponent (Default)</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af2b1-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="af2b1-106">ListByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af2b1-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="af2b1-107">GetByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af2b1-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="af2b1-108">GetByInputObjectResultType</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af2b1-109">Listebyresourceıd</span><span class="sxs-lookup"><span data-stu-id="af2b1-109">ListByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af2b1-110">Getbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="af2b1-110">GetByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af2b1-111">Getbyresourceıdresulttype</span><span class="sxs-lookup"><span data-stu-id="af2b1-111">GetByResourceIdResultType</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af2b1-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="af2b1-112">GetByComponent</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af2b1-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="af2b1-113">GetByComponentResultType</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af2b1-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="af2b1-114">DESCRIPTION</span></span>
<span data-ttu-id="af2b1-115">Get-AzDataMigrationTask cmdlet 'i, Azure veritabanı geçiş hizmeti geçiş göreviyle ilişkili özellikleri alır.</span><span class="sxs-lookup"><span data-stu-id="af2b1-115">The Get-AzDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="af2b1-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af2b1-116">EXAMPLES</span></span>

### <span data-ttu-id="af2b1-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="af2b1-117">Example 1</span></span>
```
PS C:\> Get -AzDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="af2b1-118">Yukarıdaki örnek, giriş parametresi olarak geçirilen görev adına dayalı bir Azure veritabanı geçiş hizmeti geçiş göreviyle ilişkili özellikleri almak için Get-AzDataMigrationTask cmdlet kullanımını gösterir</span><span class="sxs-lookup"><span data-stu-id="af2b1-118">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="af2b1-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="af2b1-119">Example 2</span></span>
```
PS C:\> Get -AzDataMigrationTask -Project $myProject
```

<span data-ttu-id="af2b1-120">Yukarıdaki örnek, giriş parametresi olarak geçirilen PSProject nesnesiyle ilişkili geçiş görevlerinin tümünü almak için Get-AzDataMigrationTask cmdlet kullanımını gösterir</span><span class="sxs-lookup"><span data-stu-id="af2b1-120">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="af2b1-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af2b1-121">PARAMETERS</span></span>

### <span data-ttu-id="af2b1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af2b1-122">-DefaultProfile</span></span>
<span data-ttu-id="af2b1-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af2b1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af2b1-124">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="af2b1-124">-Expand</span></span>
<span data-ttu-id="af2b1-125">Çıktıyı genişletme</span><span class="sxs-lookup"><span data-stu-id="af2b1-125">Expand output</span></span>

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

### <span data-ttu-id="af2b1-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af2b1-126">-InputObject</span></span>
<span data-ttu-id="af2b1-127">PSProject nesnesi.</span><span class="sxs-lookup"><span data-stu-id="af2b1-127">PSProject Object.</span></span>

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

### <span data-ttu-id="af2b1-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="af2b1-128">-Name</span></span>
<span data-ttu-id="af2b1-129">Görevin adı.</span><span class="sxs-lookup"><span data-stu-id="af2b1-129">The name of the task.</span></span>

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

### <span data-ttu-id="af2b1-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="af2b1-130">-ProjectName</span></span>
<span data-ttu-id="af2b1-131">Projenin adı.</span><span class="sxs-lookup"><span data-stu-id="af2b1-131">The name of the project.</span></span>

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

### <span data-ttu-id="af2b1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af2b1-132">-ResourceGroupName</span></span>
<span data-ttu-id="af2b1-133">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="af2b1-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="af2b1-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="af2b1-134">-ResourceId</span></span>
<span data-ttu-id="af2b1-135">Proje kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="af2b1-135">Project Resource Id.</span></span>

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

### <span data-ttu-id="af2b1-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="af2b1-136">-ResultType</span></span>
<span data-ttu-id="af2b1-137">Verilen sonuç türünün çıkışını genişletme.</span><span class="sxs-lookup"><span data-stu-id="af2b1-137">Expand output of given result type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput, LoginLevelOutput, AgentJobLevelOutput, Command

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af2b1-138">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="af2b1-138">-ServiceName</span></span>
<span data-ttu-id="af2b1-139">Veritabanı geçiş hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="af2b1-139">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="af2b1-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="af2b1-140">-TaskType</span></span>
<span data-ttu-id="af2b1-141">Göreve göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="af2b1-141">Filter by TaskType.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum]
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af2b1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af2b1-142">CommonParameters</span></span>
<span data-ttu-id="af2b1-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af2b1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af2b1-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af2b1-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af2b1-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af2b1-145">INPUTS</span></span>

### <span data-ttu-id="af2b1-146">Microsoft. Azure. Commands. DataMigration. modeller. PSProject</span><span class="sxs-lookup"><span data-stu-id="af2b1-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="af2b1-147">System. String</span><span class="sxs-lookup"><span data-stu-id="af2b1-147">System.String</span></span>

## <span data-ttu-id="af2b1-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af2b1-148">OUTPUTS</span></span>

### <span data-ttu-id="af2b1-149">Microsoft. Azure. Commands. DataMigration. modeller. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="af2b1-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="af2b1-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af2b1-150">NOTES</span></span>

## <span data-ttu-id="af2b1-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af2b1-151">RELATED LINKS</span></span>
