---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/remove-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
ms.openlocfilehash: 4bbca5286af5b9a0fe616134b8e9e816bd9eb68f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095966"
---
# <span data-ttu-id="d2566-101">Remove-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="d2566-101">Remove-AzIotCentralApp</span></span>

## <span data-ttu-id="d2566-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2566-102">SYNOPSIS</span></span>
<span data-ttu-id="d2566-103">IoT Merkezi uygulamasını siler.</span><span class="sxs-lookup"><span data-stu-id="d2566-103">Deletes an IoT Central Application.</span></span>

## <span data-ttu-id="d2566-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2566-104">SYNTAX</span></span>

### <span data-ttu-id="d2566-105">Resourceıdparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d2566-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzIotCentralApp [-PassThru] -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2566-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="d2566-106">InputObjectParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2566-107">Interactiveıotmerkezileştirme Parametrekümesi</span><span class="sxs-lookup"><span data-stu-id="d2566-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2566-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2566-108">DESCRIPTION</span></span>
<span data-ttu-id="d2566-109">Var olan bir IoT Merkezi uygulamasını siler.</span><span class="sxs-lookup"><span data-stu-id="d2566-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="d2566-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2566-110">EXAMPLES</span></span>

### <span data-ttu-id="d2566-111">Örnek 1 Delete ve IoT Merkezi uygulaması</span><span class="sxs-lookup"><span data-stu-id="d2566-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="d2566-112">Sağlanan IoT Merkezi uygulamasını siler.</span><span class="sxs-lookup"><span data-stu-id="d2566-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="d2566-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2566-113">PARAMETERS</span></span>

### <span data-ttu-id="d2566-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="d2566-114">-AsJob</span></span>
<span data-ttu-id="d2566-115">Cmdlet 'i arka planda iş olarak çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="d2566-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="d2566-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2566-116">-DefaultProfile</span></span>
<span data-ttu-id="d2566-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d2566-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2566-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2566-118">-InputObject</span></span>
<span data-ttu-id="d2566-119">IoT Merkezi uygulama giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d2566-119">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2566-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="d2566-120">-Name</span></span>
<span data-ttu-id="d2566-121">IoT Merkezi uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="d2566-121">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2566-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d2566-122">-PassThru</span></span>
<span data-ttu-id="d2566-123">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="d2566-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d2566-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2566-124">-ResourceGroupName</span></span>
<span data-ttu-id="d2566-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d2566-125">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2566-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d2566-126">-ResourceId</span></span>
<span data-ttu-id="d2566-127">IoT Merkezi uygulama kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="d2566-127">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2566-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="d2566-128">-Confirm</span></span>
<span data-ttu-id="d2566-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d2566-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2566-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2566-130">-WhatIf</span></span>
<span data-ttu-id="d2566-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d2566-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2566-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d2566-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2566-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2566-133">CommonParameters</span></span>
<span data-ttu-id="d2566-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2566-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2566-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2566-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2566-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2566-136">INPUTS</span></span>

### <span data-ttu-id="d2566-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d2566-137">System.String</span></span>

### <span data-ttu-id="d2566-138">Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="d2566-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="d2566-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2566-139">OUTPUTS</span></span>

### <span data-ttu-id="d2566-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d2566-140">System.Boolean</span></span>

## <span data-ttu-id="d2566-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2566-141">NOTES</span></span>

## <span data-ttu-id="d2566-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2566-142">RELATED LINKS</span></span>
