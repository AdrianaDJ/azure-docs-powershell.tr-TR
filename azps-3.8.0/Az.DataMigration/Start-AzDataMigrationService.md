---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Start-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
ms.openlocfilehash: 2b5c24b3745007cb3a2f48432609490bd38a4186
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937372"
---
# <span data-ttu-id="ea9c7-101">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ea9c7-101">Start-AzDataMigrationService</span></span>

## <span data-ttu-id="ea9c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea9c7-102">SYNOPSIS</span></span>
<span data-ttu-id="ea9c7-103">Bir Azure veritabanı geçiş hizmeti örneğini durdurulmuş durumda başlatır.</span><span class="sxs-lookup"><span data-stu-id="ea9c7-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="ea9c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea9c7-104">SYNTAX</span></span>

### <span data-ttu-id="ea9c7-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ea9c7-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea9c7-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="ea9c7-106">ComponentObjectParameterSet</span></span>
```
Start-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea9c7-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ea9c7-107">ResourceIdParameterSet</span></span>
```
Start-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea9c7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea9c7-108">DESCRIPTION</span></span>
<span data-ttu-id="ea9c7-109">Start-AzDataMigrationService cmdlet 'i, Azure veritabanı geçiş hizmeti 'nin bir örneğini durdurulmuş durumda başlatır.</span><span class="sxs-lookup"><span data-stu-id="ea9c7-109">The Start-AzDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="ea9c7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea9c7-110">EXAMPLES</span></span>

### <span data-ttu-id="ea9c7-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ea9c7-111">Example 1</span></span>
```
PS C:\> Start-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="ea9c7-112">Yukarıdaki örnek, giriş olarak geçirilen hizmet adına dayalı olarak durdurulmuş bir durumda test hizmeti adındaki bir Azure veritabanı geçiş hizmeti örneğini başlatır</span><span class="sxs-lookup"><span data-stu-id="ea9c7-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="ea9c7-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ea9c7-113">Example 2</span></span>
```
PS C:\> Start-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="ea9c7-114">Yukarıdaki örnek, giriş parametresi olarak geçirilen PSDataMigrationService tabanlı bir Azure veritabanı geçiş hizmeti başlatır</span><span class="sxs-lookup"><span data-stu-id="ea9c7-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="ea9c7-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea9c7-115">PARAMETERS</span></span>

### <span data-ttu-id="ea9c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea9c7-116">-DefaultProfile</span></span>
<span data-ttu-id="ea9c7-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ea9c7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea9c7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea9c7-118">-InputObject</span></span>
<span data-ttu-id="ea9c7-119">PSDataMigrationService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ea9c7-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="ea9c7-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="ea9c7-120">-Name</span></span>
<span data-ttu-id="ea9c7-121">Veritabanı geçiş hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="ea9c7-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="ea9c7-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ea9c7-122">-PassThru</span></span>
<span data-ttu-id="ea9c7-123">Bir doğru/yanlış döndürür.</span><span class="sxs-lookup"><span data-stu-id="ea9c7-123">Returns an true/false.</span></span>
<span data-ttu-id="ea9c7-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="ea9c7-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ea9c7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea9c7-125">-ResourceGroupName</span></span>
<span data-ttu-id="ea9c7-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ea9c7-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="ea9c7-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ea9c7-127">-ResourceId</span></span>
<span data-ttu-id="ea9c7-128">DataMigrationService kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="ea9c7-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="ea9c7-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="ea9c7-129">-Confirm</span></span>
<span data-ttu-id="ea9c7-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ea9c7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea9c7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea9c7-131">-WhatIf</span></span>
<span data-ttu-id="ea9c7-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ea9c7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea9c7-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ea9c7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea9c7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea9c7-134">CommonParameters</span></span>
<span data-ttu-id="ea9c7-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea9c7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea9c7-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea9c7-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea9c7-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea9c7-137">INPUTS</span></span>

### <span data-ttu-id="ea9c7-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ea9c7-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="ea9c7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ea9c7-139">System.String</span></span>

## <span data-ttu-id="ea9c7-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea9c7-140">OUTPUTS</span></span>

### <span data-ttu-id="ea9c7-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea9c7-141">System.Boolean</span></span>

## <span data-ttu-id="ea9c7-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea9c7-142">NOTES</span></span>

## <span data-ttu-id="ea9c7-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea9c7-143">RELATED LINKS</span></span>
