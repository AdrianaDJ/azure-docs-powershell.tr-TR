---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/start-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
ms.openlocfilehash: 03f07eaac1dbf616c78d1ca39561945b2a844b48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586708"
---
# <span data-ttu-id="431be-101">Start-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="431be-101">Start-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="431be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="431be-102">SYNOPSIS</span></span>
<span data-ttu-id="431be-103">Bir Azure veritabanı geçiş hizmeti örneğini durdurulmuş durumda başlatır.</span><span class="sxs-lookup"><span data-stu-id="431be-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="431be-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="431be-104">SYNTAX</span></span>

### <span data-ttu-id="431be-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="431be-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="431be-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="431be-106">ComponentObjectParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="431be-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="431be-107">ResourceIdParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="431be-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="431be-108">DESCRIPTION</span></span>
<span data-ttu-id="431be-109">Start-AzureRmDataMigrationService cmdlet 'i, Azure veritabanı geçiş hizmeti 'nin bir örneğini durdurulmuş durumda başlatır.</span><span class="sxs-lookup"><span data-stu-id="431be-109">The Start-AzureRmDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="431be-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="431be-110">EXAMPLES</span></span>

### <span data-ttu-id="431be-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="431be-111">Example 1</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService
```

<span data-ttu-id="431be-112">Yukarıdaki örnek, giriş olarak geçirilen hizmet adına dayalı olarak durdurulmuş bir durumda test hizmeti adındaki bir Azure veritabanı geçiş hizmeti örneğini başlatır</span><span class="sxs-lookup"><span data-stu-id="431be-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="431be-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="431be-113">Example 2</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="431be-114">Yukarıdaki örnek, giriş parametresi olarak geçirilen PSDataMigrationService tabanlı bir Azure veritabanı geçiş hizmeti başlatır</span><span class="sxs-lookup"><span data-stu-id="431be-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="431be-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="431be-115">PARAMETERS</span></span>

### <span data-ttu-id="431be-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="431be-116">-Confirm</span></span>
<span data-ttu-id="431be-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="431be-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="431be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="431be-118">-DefaultProfile</span></span>
<span data-ttu-id="431be-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="431be-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="431be-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="431be-120">-InputObject</span></span>
<span data-ttu-id="431be-121">PSDataMigrationService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="431be-121">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="431be-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="431be-122">-Name</span></span>
<span data-ttu-id="431be-123">Veri geçişi hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="431be-123">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="431be-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="431be-124">-PassThru</span></span>
<span data-ttu-id="431be-125">Bir doğru/yanlış döndürür.</span><span class="sxs-lookup"><span data-stu-id="431be-125">Returns an true/false.</span></span>
<span data-ttu-id="431be-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="431be-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="431be-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="431be-127">-ResourceGroupName</span></span>
<span data-ttu-id="431be-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="431be-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="431be-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="431be-129">-ResourceId</span></span>
<span data-ttu-id="431be-130">DataMigrationService kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="431be-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="431be-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="431be-131">-WhatIf</span></span>
<span data-ttu-id="431be-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="431be-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="431be-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="431be-133">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="431be-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="431be-134">INPUTS</span></span>

### <span data-ttu-id="431be-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="431be-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="431be-136">System. String</span><span class="sxs-lookup"><span data-stu-id="431be-136">System.String</span></span>


## <span data-ttu-id="431be-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="431be-137">OUTPUTS</span></span>

### <span data-ttu-id="431be-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="431be-138">System.Boolean</span></span>


## <span data-ttu-id="431be-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="431be-139">NOTES</span></span>

## <span data-ttu-id="431be-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="431be-140">RELATED LINKS</span></span>


