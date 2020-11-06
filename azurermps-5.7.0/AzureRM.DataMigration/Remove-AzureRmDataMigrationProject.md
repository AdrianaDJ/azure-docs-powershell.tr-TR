---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
ms.openlocfilehash: 8ec046df13302ece90e57bcb722816f2019ff2e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594083"
---
# <span data-ttu-id="bb344-101">Remove-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="bb344-101">Remove-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="bb344-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb344-102">SYNOPSIS</span></span>
<span data-ttu-id="bb344-103">Azure veritabanı geçiş hizmeti projesini Azure 'dan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bb344-103">Removes an Azure Database Migration Service project from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb344-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb344-104">SYNTAX</span></span>

### <span data-ttu-id="bb344-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bb344-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="bb344-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="bb344-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="bb344-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="bb344-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="bb344-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb344-108">DESCRIPTION</span></span>
<span data-ttu-id="bb344-109">Remove-AzureRmDataMigrationProject cmdlet 'i Azure 'dan Azure veritabanı geçiş hizmeti projesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bb344-109">The Remove-AzureRmDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="bb344-110">DeleteRunningTask parametresi sağlanırken, kaldırılmakta olan projeyle ilişkili tüm Azure veritabanı yükseltme hizmeti görevleri kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="bb344-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="bb344-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb344-111">EXAMPLES</span></span>

### <span data-ttu-id="bb344-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bb344-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="bb344-113">Yukarıdaki örnek, giriş parametresi olarak ad temelinde Azure 'dan myDMProject adlı Azure veritabanı geçiş hizmeti projesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="bb344-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="bb344-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="bb344-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="bb344-115">Yukarıdaki örnek, Azure veritabanı geçiş hizmeti projesini, PSProject nesnesini giriş parametresi olarak kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bb344-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="bb344-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb344-116">PARAMETERS</span></span>

### <span data-ttu-id="bb344-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="bb344-117">-Confirm</span></span>
<span data-ttu-id="bb344-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bb344-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb344-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb344-119">-DefaultProfile</span></span>
<span data-ttu-id="bb344-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bb344-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb344-121">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="bb344-121">-DeleteRunningTask</span></span>
<span data-ttu-id="bb344-122">Çalışan görevleri silme</span><span class="sxs-lookup"><span data-stu-id="bb344-122">Delete any running task</span></span>

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

### <span data-ttu-id="bb344-123">-Force</span><span class="sxs-lookup"><span data-stu-id="bb344-123">-Force</span></span>
<span data-ttu-id="bb344-124">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="bb344-124">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="bb344-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb344-125">-InputObject</span></span>
<span data-ttu-id="bb344-126">PSProject nesnesi.</span><span class="sxs-lookup"><span data-stu-id="bb344-126">PSProject Object.</span></span>

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

### <span data-ttu-id="bb344-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="bb344-127">-Name</span></span>
<span data-ttu-id="bb344-128">Projenin adı.</span><span class="sxs-lookup"><span data-stu-id="bb344-128">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb344-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bb344-129">-PassThru</span></span>
<span data-ttu-id="bb344-130">Bir doğru/yanlış döndürür.</span><span class="sxs-lookup"><span data-stu-id="bb344-130">Returns an true/false.</span></span>
<span data-ttu-id="bb344-131">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="bb344-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bb344-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb344-132">-ResourceGroupName</span></span>
<span data-ttu-id="bb344-133">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bb344-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="bb344-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bb344-134">-ResourceId</span></span>
<span data-ttu-id="bb344-135">Proje kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="bb344-135">Project Resource Id.</span></span>

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

### <span data-ttu-id="bb344-136">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="bb344-136">-ServiceName</span></span>
<span data-ttu-id="bb344-137">Veri geçişi hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="bb344-137">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="bb344-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb344-138">-WhatIf</span></span>
<span data-ttu-id="bb344-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bb344-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb344-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bb344-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="bb344-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb344-141">INPUTS</span></span>

### <span data-ttu-id="bb344-142">Microsoft. Azure. Commands. DataMigration. modeller. PSProject</span><span class="sxs-lookup"><span data-stu-id="bb344-142">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="bb344-143">System. String</span><span class="sxs-lookup"><span data-stu-id="bb344-143">System.String</span></span>


## <span data-ttu-id="bb344-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb344-144">OUTPUTS</span></span>

### <span data-ttu-id="bb344-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bb344-145">System.Boolean</span></span>


## <span data-ttu-id="bb344-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb344-146">NOTES</span></span>

## <span data-ttu-id="bb344-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb344-147">RELATED LINKS</span></span>

