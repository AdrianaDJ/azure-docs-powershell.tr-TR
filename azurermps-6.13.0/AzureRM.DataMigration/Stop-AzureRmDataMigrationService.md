---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Stop-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
ms.openlocfilehash: 59ec77f0c6e3a2f9389931e12ecbce155fe970bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589568"
---
# <span data-ttu-id="f333e-101">Stop-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f333e-101">Stop-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="f333e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f333e-102">SYNOPSIS</span></span>
<span data-ttu-id="f333e-103">Çalışan bir durumda olan Azure veritabanı geçiş hizmeti 'nin bir örneğini durdurur.</span><span class="sxs-lookup"><span data-stu-id="f333e-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f333e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f333e-104">SYNTAX</span></span>

### <span data-ttu-id="f333e-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f333e-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f333e-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="f333e-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f333e-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="f333e-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f333e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f333e-108">DESCRIPTION</span></span>
<span data-ttu-id="f333e-109">Stop-AzureRmDataMigrationService cmdlet 'i, çalışan bir durumda olan Azure veritabanı geçiş hizmeti 'nin bir örneğini durdurur.</span><span class="sxs-lookup"><span data-stu-id="f333e-109">The Stop-AzureRmDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="f333e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f333e-110">EXAMPLES</span></span>

### <span data-ttu-id="f333e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f333e-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="f333e-112">Yukarıdaki örnek, giriş parametresi olarak geçirilen hizmet adına dayanan TestService adındaki bir Azure veritabanı geçiş hizmeti örneğini durdurur</span><span class="sxs-lookup"><span data-stu-id="f333e-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="f333e-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f333e-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="f333e-114">Yukarıdaki örnek, giriş parametresi olarak geçirilen PSDataMigrationService nesnesini temel alan Azure veritabanı geçiş hizmeti örneğini durdurur.</span><span class="sxs-lookup"><span data-stu-id="f333e-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="f333e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f333e-115">PARAMETERS</span></span>

### <span data-ttu-id="f333e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f333e-116">-DefaultProfile</span></span>
<span data-ttu-id="f333e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f333e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f333e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f333e-118">-InputObject</span></span>
<span data-ttu-id="f333e-119">PSDataMigrationService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f333e-119">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f333e-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="f333e-120">-Name</span></span>
<span data-ttu-id="f333e-121">Veritabanı geçiş hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="f333e-121">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f333e-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f333e-122">-PassThru</span></span>
<span data-ttu-id="f333e-123">Bir doğru/yanlış döndürür.</span><span class="sxs-lookup"><span data-stu-id="f333e-123">Returns an true/false.</span></span>
<span data-ttu-id="f333e-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="f333e-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f333e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f333e-125">-ResourceGroupName</span></span>
<span data-ttu-id="f333e-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f333e-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="f333e-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f333e-127">-ResourceId</span></span>
<span data-ttu-id="f333e-128">DataMigrationService kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="f333e-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="f333e-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="f333e-129">-Confirm</span></span>
<span data-ttu-id="f333e-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f333e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f333e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f333e-131">-WhatIf</span></span>
<span data-ttu-id="f333e-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f333e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f333e-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f333e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f333e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f333e-134">CommonParameters</span></span>
<span data-ttu-id="f333e-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f333e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f333e-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f333e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f333e-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f333e-137">INPUTS</span></span>

### <span data-ttu-id="f333e-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f333e-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="f333e-139">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f333e-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="f333e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f333e-140">System.String</span></span>

## <span data-ttu-id="f333e-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f333e-141">OUTPUTS</span></span>

### <span data-ttu-id="f333e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f333e-142">System.Boolean</span></span>

## <span data-ttu-id="f333e-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f333e-143">NOTES</span></span>

## <span data-ttu-id="f333e-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f333e-144">RELATED LINKS</span></span>
