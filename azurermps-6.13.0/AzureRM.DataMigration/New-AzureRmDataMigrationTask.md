---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
ms.openlocfilehash: 8352f7a63e40986e27c4b521dca58aaf003679bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593674"
---
# <span data-ttu-id="7881f-101">New-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="7881f-101">New-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="7881f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7881f-102">SYNOPSIS</span></span>
<span data-ttu-id="7881f-103">Azure veritabanı geçiş hizmeti 'nde veri geçişi görevini oluşturur ve başlatır.</span><span class="sxs-lookup"><span data-stu-id="7881f-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7881f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7881f-104">SYNTAX</span></span>

### <span data-ttu-id="7881f-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7881f-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7881f-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="7881f-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7881f-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="7881f-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7881f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7881f-108">DESCRIPTION</span></span>
<span data-ttu-id="7881f-109">New-AzureRmDataMigrationTask cmdlet 'i veri geçişi görevini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7881f-109">The New-AzureRmDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="7881f-110">Bu cmdlet, görev türü Numaralandırıcı, Azure Kaynak grubu, ilişkili Azure veritabanı geçiş hizmeti ve Project 'in adını giriş olarak alır.</span><span class="sxs-lookup"><span data-stu-id="7881f-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="7881f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7881f-111">EXAMPLES</span></span>

### <span data-ttu-id="7881f-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7881f-112">Example 1</span></span>
```
PS C:\> New-AzureRmDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs
```

<span data-ttu-id="7881f-113">Bu örnek komut dosyası, Myvseçmsproject adlı projede MyMigrationTask adlı yeni bir veri taşıma görevinin ve TestService adlı hizmetin nasıl oluşturulduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="7881f-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="7881f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7881f-114">PARAMETERS</span></span>

### <span data-ttu-id="7881f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7881f-115">-DefaultProfile</span></span>
<span data-ttu-id="7881f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7881f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7881f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7881f-117">-InputObject</span></span>
<span data-ttu-id="7881f-118">PSProject nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7881f-118">PSProject Object.</span></span>

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

### <span data-ttu-id="7881f-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="7881f-119">-Name</span></span>
<span data-ttu-id="7881f-120">Görevin adı.</span><span class="sxs-lookup"><span data-stu-id="7881f-120">The name of the task.</span></span>

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

### <span data-ttu-id="7881f-121">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="7881f-121">-ProjectName</span></span>
<span data-ttu-id="7881f-122">Projenin adı.</span><span class="sxs-lookup"><span data-stu-id="7881f-122">The name of the project.</span></span>

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

### <span data-ttu-id="7881f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7881f-123">-ResourceGroupName</span></span>
<span data-ttu-id="7881f-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7881f-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="7881f-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7881f-125">-ResourceId</span></span>
<span data-ttu-id="7881f-126">Proje kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="7881f-126">Project Resource Id.</span></span>

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

### <span data-ttu-id="7881f-127">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="7881f-127">-ServiceName</span></span>
<span data-ttu-id="7881f-128">Veritabanı geçiş hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="7881f-128">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="7881f-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="7881f-129">-TaskType</span></span>
<span data-ttu-id="7881f-130">Görev türü.</span><span class="sxs-lookup"><span data-stu-id="7881f-130">Task Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7881f-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="7881f-131">-Confirm</span></span>
<span data-ttu-id="7881f-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7881f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7881f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7881f-133">-WhatIf</span></span>
<span data-ttu-id="7881f-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7881f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7881f-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7881f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7881f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7881f-136">CommonParameters</span></span>
<span data-ttu-id="7881f-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7881f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7881f-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7881f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7881f-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7881f-139">INPUTS</span></span>

### <span data-ttu-id="7881f-140">Microsoft. Azure. Commands. DataMigration. modeller. PSProject</span><span class="sxs-lookup"><span data-stu-id="7881f-140">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="7881f-141">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7881f-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="7881f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="7881f-142">System.String</span></span>

## <span data-ttu-id="7881f-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7881f-143">OUTPUTS</span></span>

### <span data-ttu-id="7881f-144">Microsoft. Azure. Commands. DataMigration. modeller. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="7881f-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="7881f-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7881f-145">NOTES</span></span>

## <span data-ttu-id="7881f-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7881f-146">RELATED LINKS</span></span>
