---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
ms.openlocfilehash: bcc1c39af722d5f12c333152e8458228f583a842
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098045"
---
# <span data-ttu-id="b6879-101">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="b6879-101">Get-AzDataMigrationTask</span></span>

## <span data-ttu-id="b6879-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6879-102">SYNOPSIS</span></span>
<span data-ttu-id="b6879-103">Bir Azure veritabanı geçiş hizmeti geçiş göreviyle ilişkili PSProjectTask nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="b6879-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="b6879-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6879-104">SYNTAX</span></span>

### <span data-ttu-id="b6879-105">ListByComponent (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b6879-105">ListByComponent (Default)</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6879-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="b6879-106">ListByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6879-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="b6879-107">GetByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6879-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="b6879-108">GetByInputObjectResultType</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6879-109">Listebyresourceıd</span><span class="sxs-lookup"><span data-stu-id="b6879-109">ListByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6879-110">Getbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="b6879-110">GetByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6879-111">Getbyresourceıdresulttype</span><span class="sxs-lookup"><span data-stu-id="b6879-111">GetByResourceIdResultType</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6879-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="b6879-112">GetByComponent</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6879-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="b6879-113">GetByComponentResultType</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6879-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6879-114">DESCRIPTION</span></span>
<span data-ttu-id="b6879-115">Get-AzDataMigrationTask cmdlet 'i, Azure veritabanı geçiş hizmeti geçiş göreviyle ilişkili özellikleri alır.</span><span class="sxs-lookup"><span data-stu-id="b6879-115">The Get-AzDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="b6879-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6879-116">EXAMPLES</span></span>

### <span data-ttu-id="b6879-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b6879-117">Example 1</span></span>
```
PS C:\> Get -AzDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="b6879-118">Yukarıdaki örnek, giriş parametresi olarak geçirilen görev adına dayalı bir Azure veritabanı geçiş hizmeti geçiş göreviyle ilişkili özellikleri almak için Get-AzDataMigrationTask cmdlet kullanımını gösterir</span><span class="sxs-lookup"><span data-stu-id="b6879-118">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="b6879-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b6879-119">Example 2</span></span>
```
PS C:\> Get -AzDataMigrationTask -Project $myProject
```

<span data-ttu-id="b6879-120">Yukarıdaki örnek, giriş parametresi olarak geçirilen PSProject nesnesiyle ilişkili geçiş görevlerinin tümünü almak için Get-AzDataMigrationTask cmdlet kullanımını gösterir</span><span class="sxs-lookup"><span data-stu-id="b6879-120">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="b6879-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6879-121">PARAMETERS</span></span>

### <span data-ttu-id="b6879-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6879-122">-DefaultProfile</span></span>
<span data-ttu-id="b6879-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b6879-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6879-124">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="b6879-124">-Expand</span></span>
<span data-ttu-id="b6879-125">Çıktıyı genişletme</span><span class="sxs-lookup"><span data-stu-id="b6879-125">Expand output</span></span>

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

### <span data-ttu-id="b6879-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6879-126">-InputObject</span></span>
<span data-ttu-id="b6879-127">PSProject nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b6879-127">PSProject Object.</span></span>

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

### <span data-ttu-id="b6879-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="b6879-128">-Name</span></span>
<span data-ttu-id="b6879-129">Görevin adı.</span><span class="sxs-lookup"><span data-stu-id="b6879-129">The name of the task.</span></span>

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

### <span data-ttu-id="b6879-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="b6879-130">-ProjectName</span></span>
<span data-ttu-id="b6879-131">Projenin adı.</span><span class="sxs-lookup"><span data-stu-id="b6879-131">The name of the project.</span></span>

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

### <span data-ttu-id="b6879-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6879-132">-ResourceGroupName</span></span>
<span data-ttu-id="b6879-133">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b6879-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="b6879-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b6879-134">-ResourceId</span></span>
<span data-ttu-id="b6879-135">Proje kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="b6879-135">Project Resource Id.</span></span>

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

### <span data-ttu-id="b6879-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="b6879-136">-ResultType</span></span>
<span data-ttu-id="b6879-137">Verilen sonuç türünün çıkışını genişletme.</span><span class="sxs-lookup"><span data-stu-id="b6879-137">Expand output of given result type.</span></span>

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

### <span data-ttu-id="b6879-138">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="b6879-138">-ServiceName</span></span>
<span data-ttu-id="b6879-139">Veritabanı geçiş hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="b6879-139">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="b6879-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="b6879-140">-TaskType</span></span>
<span data-ttu-id="b6879-141">Göreve göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="b6879-141">Filter by TaskType.</span></span>

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

### <span data-ttu-id="b6879-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6879-142">CommonParameters</span></span>
<span data-ttu-id="b6879-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6879-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6879-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6879-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6879-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6879-145">INPUTS</span></span>

### <span data-ttu-id="b6879-146">Microsoft. Azure. Commands. DataMigration. modeller. PSProject</span><span class="sxs-lookup"><span data-stu-id="b6879-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="b6879-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b6879-147">System.String</span></span>

## <span data-ttu-id="b6879-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6879-148">OUTPUTS</span></span>

### <span data-ttu-id="b6879-149">Microsoft. Azure. Commands. DataMigration. modeller. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="b6879-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="b6879-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6879-150">NOTES</span></span>

## <span data-ttu-id="b6879-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6879-151">RELATED LINKS</span></span>
