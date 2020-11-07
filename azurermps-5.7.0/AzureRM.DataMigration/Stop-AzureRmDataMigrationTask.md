---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/stop-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationTask.md
ms.openlocfilehash: 7cf68cd27125580c6f0e57a7849c1fadc8cb47fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762863"
---
# <span data-ttu-id="d2e8a-101">Stop-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="d2e8a-101">Stop-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="d2e8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e8a-103">Çalışmakta olan bir Azure veritabanı geçiş hizmeti görevini durdurur.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2e8a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2e8a-104">SYNTAX</span></span>

### <span data-ttu-id="d2e8a-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d2e8a-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d2e8a-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="d2e8a-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d2e8a-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d2e8a-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="d2e8a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2e8a-108">DESCRIPTION</span></span>
<span data-ttu-id="d2e8a-109">Stop-AzureRmDataMigrationTask cmdlet, çalışma durumundaki veritabanı geçişi etkinliğini durdurur.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-109">Stop-AzureRmDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="d2e8a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2e8a-110">EXAMPLES</span></span>

### <span data-ttu-id="d2e8a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d2e8a-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="d2e8a-112">Yukarıdaki örnek, myDMSTask adlı Project Myvseçmsproject ve Azure veritabanı geçiş hizmeti</span><span class="sxs-lookup"><span data-stu-id="d2e8a-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="d2e8a-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d2e8a-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="d2e8a-114">Yukarıdaki örnek Azure veritabanı geçiş hizmeti görevini</span><span class="sxs-lookup"><span data-stu-id="d2e8a-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="d2e8a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2e8a-115">PARAMETERS</span></span>

### <span data-ttu-id="d2e8a-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="d2e8a-116">-Confirm</span></span>
<span data-ttu-id="d2e8a-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2e8a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e8a-118">-DefaultProfile</span></span>
<span data-ttu-id="d2e8a-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2e8a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2e8a-120">-InputObject</span></span>
<span data-ttu-id="d2e8a-121">PSProjectTask nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-121">PSProjectTask Object.</span></span>

```yaml
Type: PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e8a-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="d2e8a-122">-Name</span></span>
<span data-ttu-id="d2e8a-123">Görevin adı.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-123">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e8a-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d2e8a-124">-PassThru</span></span>
<span data-ttu-id="d2e8a-125">Bir doğru/yanlış döndürür.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-125">Returns an true/false.</span></span>
<span data-ttu-id="d2e8a-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e8a-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="d2e8a-127">-ProjectName</span></span>
<span data-ttu-id="d2e8a-128">Projenin adı.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-128">The name of the project.</span></span>

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

### <span data-ttu-id="d2e8a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2e8a-129">-ResourceGroupName</span></span>
<span data-ttu-id="d2e8a-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-130">The name of the resource group .</span></span>

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

### <span data-ttu-id="d2e8a-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d2e8a-131">-ResourceId</span></span>
<span data-ttu-id="d2e8a-132">ProjectTask kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-132">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="d2e8a-133">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="d2e8a-133">-ServiceName</span></span>
<span data-ttu-id="d2e8a-134">Veri geçişi hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-134">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="d2e8a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2e8a-135">-WhatIf</span></span>
<span data-ttu-id="d2e8a-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2e8a-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d2e8a-137">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="d2e8a-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2e8a-138">INPUTS</span></span>

### <span data-ttu-id="d2e8a-139">Microsoft. Azure. Commands. DataMigration. modeller. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="d2e8a-139">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="d2e8a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d2e8a-140">System.String</span></span>


## <span data-ttu-id="d2e8a-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2e8a-141">OUTPUTS</span></span>

### <span data-ttu-id="d2e8a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d2e8a-142">System.Boolean</span></span>


## <span data-ttu-id="d2e8a-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2e8a-143">NOTES</span></span>

## <span data-ttu-id="d2e8a-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2e8a-144">RELATED LINKS</span></span>

