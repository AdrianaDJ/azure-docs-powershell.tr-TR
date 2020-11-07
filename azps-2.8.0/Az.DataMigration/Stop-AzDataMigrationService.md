---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
ms.openlocfilehash: b838cef6b72c783c8a9252df1e448e27bd100e36
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752230"
---
# <span data-ttu-id="c0306-101">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="c0306-101">Stop-AzDataMigrationService</span></span>

## <span data-ttu-id="c0306-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0306-102">SYNOPSIS</span></span>
<span data-ttu-id="c0306-103">Çalışan bir durumda olan Azure veritabanı geçiş hizmeti 'nin bir örneğini durdurur.</span><span class="sxs-lookup"><span data-stu-id="c0306-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="c0306-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0306-104">SYNTAX</span></span>

### <span data-ttu-id="c0306-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c0306-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0306-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="c0306-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0306-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c0306-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0306-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0306-108">DESCRIPTION</span></span>
<span data-ttu-id="c0306-109">Stop-AzDataMigrationService cmdlet 'i, çalışan bir durumda olan Azure veritabanı geçiş hizmeti 'nin bir örneğini durdurur.</span><span class="sxs-lookup"><span data-stu-id="c0306-109">The Stop-AzDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="c0306-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0306-110">EXAMPLES</span></span>

### <span data-ttu-id="c0306-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c0306-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="c0306-112">Yukarıdaki örnek, giriş parametresi olarak geçirilen hizmet adına dayanan TestService adındaki bir Azure veritabanı geçiş hizmeti örneğini durdurur</span><span class="sxs-lookup"><span data-stu-id="c0306-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="c0306-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c0306-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="c0306-114">Yukarıdaki örnek, giriş parametresi olarak geçirilen PSDataMigrationService nesnesini temel alan Azure veritabanı geçiş hizmeti örneğini durdurur.</span><span class="sxs-lookup"><span data-stu-id="c0306-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="c0306-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0306-115">PARAMETERS</span></span>

### <span data-ttu-id="c0306-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0306-116">-DefaultProfile</span></span>
<span data-ttu-id="c0306-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c0306-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0306-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0306-118">-InputObject</span></span>
<span data-ttu-id="c0306-119">PSDataMigrationService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c0306-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="c0306-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="c0306-120">-Name</span></span>
<span data-ttu-id="c0306-121">Veritabanı geçiş hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="c0306-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="c0306-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c0306-122">-PassThru</span></span>
<span data-ttu-id="c0306-123">Bir doğru/yanlış döndürür.</span><span class="sxs-lookup"><span data-stu-id="c0306-123">Returns an true/false.</span></span>
<span data-ttu-id="c0306-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="c0306-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c0306-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0306-125">-ResourceGroupName</span></span>
<span data-ttu-id="c0306-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c0306-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="c0306-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c0306-127">-ResourceId</span></span>
<span data-ttu-id="c0306-128">DataMigrationService kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="c0306-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="c0306-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="c0306-129">-Confirm</span></span>
<span data-ttu-id="c0306-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c0306-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0306-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0306-131">-WhatIf</span></span>
<span data-ttu-id="c0306-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c0306-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0306-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c0306-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0306-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0306-134">CommonParameters</span></span>
<span data-ttu-id="c0306-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0306-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0306-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0306-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0306-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0306-137">INPUTS</span></span>

### <span data-ttu-id="c0306-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="c0306-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="c0306-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c0306-139">System.String</span></span>

## <span data-ttu-id="c0306-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0306-140">OUTPUTS</span></span>

### <span data-ttu-id="c0306-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c0306-141">System.Boolean</span></span>

## <span data-ttu-id="c0306-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0306-142">NOTES</span></span>

## <span data-ttu-id="c0306-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0306-143">RELATED LINKS</span></span>
