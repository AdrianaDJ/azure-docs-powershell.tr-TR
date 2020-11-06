---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Start-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
ms.openlocfilehash: a8440ddc7249068486f94c30e28e1b1be2e2413e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594900"
---
# <span data-ttu-id="dba7f-101">Start-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="dba7f-101">Start-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="dba7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dba7f-102">SYNOPSIS</span></span>
<span data-ttu-id="dba7f-103">Bir Azure veritabanı geçiş hizmeti örneğini durdurulmuş durumda başlatır.</span><span class="sxs-lookup"><span data-stu-id="dba7f-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dba7f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dba7f-104">SYNTAX</span></span>

### <span data-ttu-id="dba7f-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dba7f-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dba7f-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="dba7f-106">ComponentObjectParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dba7f-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="dba7f-107">ResourceIdParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dba7f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="dba7f-108">DESCRIPTION</span></span>
<span data-ttu-id="dba7f-109">Start-AzureRmDataMigrationService cmdlet 'i, Azure veritabanı geçiş hizmeti 'nin bir örneğini durdurulmuş durumda başlatır.</span><span class="sxs-lookup"><span data-stu-id="dba7f-109">The Start-AzureRmDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="dba7f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dba7f-110">EXAMPLES</span></span>

### <span data-ttu-id="dba7f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dba7f-111">Example 1</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="dba7f-112">Yukarıdaki örnek, giriş olarak geçirilen hizmet adına dayalı olarak durdurulmuş bir durumda test hizmeti adındaki bir Azure veritabanı geçiş hizmeti örneğini başlatır</span><span class="sxs-lookup"><span data-stu-id="dba7f-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="dba7f-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="dba7f-113">Example 2</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="dba7f-114">Yukarıdaki örnek, giriş parametresi olarak geçirilen PSDataMigrationService tabanlı bir Azure veritabanı geçiş hizmeti başlatır</span><span class="sxs-lookup"><span data-stu-id="dba7f-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="dba7f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dba7f-115">PARAMETERS</span></span>

### <span data-ttu-id="dba7f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dba7f-116">-DefaultProfile</span></span>
<span data-ttu-id="dba7f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dba7f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dba7f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dba7f-118">-InputObject</span></span>
<span data-ttu-id="dba7f-119">PSDataMigrationService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="dba7f-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="dba7f-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="dba7f-120">-Name</span></span>
<span data-ttu-id="dba7f-121">Veritabanı geçiş hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="dba7f-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="dba7f-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="dba7f-122">-PassThru</span></span>
<span data-ttu-id="dba7f-123">Bir doğru/yanlış döndürür.</span><span class="sxs-lookup"><span data-stu-id="dba7f-123">Returns an true/false.</span></span>
<span data-ttu-id="dba7f-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="dba7f-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dba7f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dba7f-125">-ResourceGroupName</span></span>
<span data-ttu-id="dba7f-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="dba7f-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="dba7f-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="dba7f-127">-ResourceId</span></span>
<span data-ttu-id="dba7f-128">DataMigrationService kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="dba7f-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="dba7f-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="dba7f-129">-Confirm</span></span>
<span data-ttu-id="dba7f-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dba7f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dba7f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dba7f-131">-WhatIf</span></span>
<span data-ttu-id="dba7f-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dba7f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dba7f-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dba7f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dba7f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba7f-134">CommonParameters</span></span>
<span data-ttu-id="dba7f-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dba7f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba7f-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dba7f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba7f-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dba7f-137">INPUTS</span></span>

### <span data-ttu-id="dba7f-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="dba7f-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="dba7f-139">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dba7f-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="dba7f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="dba7f-140">System.String</span></span>

## <span data-ttu-id="dba7f-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dba7f-141">OUTPUTS</span></span>

### <span data-ttu-id="dba7f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dba7f-142">System.Boolean</span></span>

## <span data-ttu-id="dba7f-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dba7f-143">NOTES</span></span>

## <span data-ttu-id="dba7f-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dba7f-144">RELATED LINKS</span></span>
