---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/stop-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
ms.openlocfilehash: 9a3028e019d3873105df079b67652f2157137ce2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594963"
---
# <span data-ttu-id="04565-101">Stop-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="04565-101">Stop-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="04565-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04565-102">SYNOPSIS</span></span>
<span data-ttu-id="04565-103">Çalışan bir durumda olan Azure veritabanı geçiş hizmeti 'nin bir örneğini durdurur.</span><span class="sxs-lookup"><span data-stu-id="04565-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04565-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="04565-104">SYNTAX</span></span>

### <span data-ttu-id="04565-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="04565-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="04565-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="04565-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="04565-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="04565-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="04565-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="04565-108">DESCRIPTION</span></span>
<span data-ttu-id="04565-109">Stop-AzureRmDataMigrationService cmdlet 'i, çalışan bir durumda olan Azure veritabanı geçiş hizmeti 'nin bir örneğini durdurur.</span><span class="sxs-lookup"><span data-stu-id="04565-109">The Stop-AzureRmDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="04565-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="04565-110">EXAMPLES</span></span>

### <span data-ttu-id="04565-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="04565-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService

```
<span data-ttu-id="04565-112">Yukarıdaki örnek, giriş parametresi olarak geçirilen hizmet adına dayanan TestService adındaki bir Azure veritabanı geçiş hizmeti örneğini durdurur</span><span class="sxs-lookup"><span data-stu-id="04565-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="04565-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="04565-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -InputObject $TestService

```
<span data-ttu-id="04565-114">Yukarıdaki örnek, giriş parametresi olarak geçirilen PSDataMigrationService nesnesini temel alan Azure veritabanı geçiş hizmeti örneğini durdurur.</span><span class="sxs-lookup"><span data-stu-id="04565-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>



## <span data-ttu-id="04565-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="04565-115">PARAMETERS</span></span>

### <span data-ttu-id="04565-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="04565-116">-Confirm</span></span>
<span data-ttu-id="04565-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="04565-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04565-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04565-118">-DefaultProfile</span></span>
<span data-ttu-id="04565-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="04565-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04565-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04565-120">-InputObject</span></span>
<span data-ttu-id="04565-121">PSDataMigrationService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="04565-121">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="04565-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="04565-122">-Name</span></span>
<span data-ttu-id="04565-123">Veri geçişi hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="04565-123">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="04565-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="04565-124">-PassThru</span></span>
<span data-ttu-id="04565-125">Bir doğru/yanlış döndürür.</span><span class="sxs-lookup"><span data-stu-id="04565-125">Returns an true/false.</span></span>
<span data-ttu-id="04565-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="04565-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="04565-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04565-127">-ResourceGroupName</span></span>
<span data-ttu-id="04565-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="04565-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="04565-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="04565-129">-ResourceId</span></span>
<span data-ttu-id="04565-130">DataMigrationService kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="04565-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="04565-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04565-131">-WhatIf</span></span>
<span data-ttu-id="04565-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="04565-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04565-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="04565-133">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="04565-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="04565-134">INPUTS</span></span>

### <span data-ttu-id="04565-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="04565-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="04565-136">System. String</span><span class="sxs-lookup"><span data-stu-id="04565-136">System.String</span></span>


## <span data-ttu-id="04565-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="04565-137">OUTPUTS</span></span>

### <span data-ttu-id="04565-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04565-138">System.Boolean</span></span>


## <span data-ttu-id="04565-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="04565-139">NOTES</span></span>

## <span data-ttu-id="04565-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="04565-140">RELATED LINKS</span></span>

