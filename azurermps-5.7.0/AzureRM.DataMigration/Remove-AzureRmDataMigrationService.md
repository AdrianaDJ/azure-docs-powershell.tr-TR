---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
ms.openlocfilehash: dde0044642f81c098358cd86cabe8c066240a215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592133"
---
# <span data-ttu-id="42e4d-101">Remove-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="42e4d-101">Remove-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="42e4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42e4d-102">SYNOPSIS</span></span>
<span data-ttu-id="42e4d-103">Azure veritabanı geçiş hizmeti 'nin bir örneğini Azure 'dan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="42e4d-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42e4d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42e4d-104">SYNTAX</span></span>

### <span data-ttu-id="42e4d-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="42e4d-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="42e4d-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="42e4d-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="42e4d-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="42e4d-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="42e4d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="42e4d-108">DESCRIPTION</span></span>
<span data-ttu-id="42e4d-109">Remove-AzureRmDataMigrationService cmdlet 'i Azure veritabanı geçiş hizmeti 'nin Azure 'dan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="42e4d-109">The Remove-AzureRmDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="42e4d-110">DeleteRunningTask parametresi sağlanırken, kaldırılmakta olan hizmetle ilişkili tüm Azure veritabanı geçiş hizmeti görevleri kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="42e4d-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="42e4d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42e4d-111">EXAMPLES</span></span>

### <span data-ttu-id="42e4d-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="42e4d-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService
```

<span data-ttu-id="42e4d-113">Yukarıdaki örnek, MyResourceGroup adlı bir Azure Kaynak grubunda bulunan TestService adındaki bir Azure veritabanı geçiş hizmeti örneğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="42e4d-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="42e4d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42e4d-114">PARAMETERS</span></span>

### <span data-ttu-id="42e4d-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="42e4d-115">-Confirm</span></span>
<span data-ttu-id="42e4d-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="42e4d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42e4d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42e4d-117">-DefaultProfile</span></span>
<span data-ttu-id="42e4d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="42e4d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42e4d-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="42e4d-119">-DeleteRunningTask</span></span>
<span data-ttu-id="42e4d-120">Çalışan görevleri silme</span><span class="sxs-lookup"><span data-stu-id="42e4d-120">Delete any running task</span></span>

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

### <span data-ttu-id="42e4d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="42e4d-121">-Force</span></span>
<span data-ttu-id="42e4d-122">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="42e4d-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="42e4d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42e4d-123">-InputObject</span></span>
<span data-ttu-id="42e4d-124">PSDataMigrationService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="42e4d-124">PSDataMigrationService Object.</span></span>

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42e4d-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="42e4d-125">-Name</span></span>
<span data-ttu-id="42e4d-126">Veri taşıma hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="42e4d-126">The name of the Data Migration Service.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e4d-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="42e4d-127">-PassThru</span></span>
<span data-ttu-id="42e4d-128">Bir doğru/yanlış döndürür.</span><span class="sxs-lookup"><span data-stu-id="42e4d-128">Returns an true/false.</span></span>
<span data-ttu-id="42e4d-129">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="42e4d-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="42e4d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42e4d-130">-ResourceGroupName</span></span>
<span data-ttu-id="42e4d-131">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="42e4d-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="42e4d-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="42e4d-132">-ResourceId</span></span>
<span data-ttu-id="42e4d-133">DataMigrationService kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="42e4d-133">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="42e4d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42e4d-134">-WhatIf</span></span>
<span data-ttu-id="42e4d-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="42e4d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42e4d-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="42e4d-136">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="42e4d-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42e4d-137">INPUTS</span></span>

### <span data-ttu-id="42e4d-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="42e4d-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="42e4d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="42e4d-139">System.String</span></span>


## <span data-ttu-id="42e4d-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42e4d-140">OUTPUTS</span></span>

### <span data-ttu-id="42e4d-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="42e4d-141">System.Boolean</span></span>


## <span data-ttu-id="42e4d-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42e4d-142">NOTES</span></span>

## <span data-ttu-id="42e4d-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42e4d-143">RELATED LINKS</span></span>


