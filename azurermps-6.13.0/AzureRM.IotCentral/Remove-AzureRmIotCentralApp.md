---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/remove-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Remove-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Remove-AzureRmIotCentralApp.md
ms.openlocfilehash: c8a2f32b82a6111c1117a4134f0f7fe8b96a966f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594889"
---
# <span data-ttu-id="d557d-101">Remove-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="d557d-101">Remove-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="d557d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d557d-102">SYNOPSIS</span></span>
<span data-ttu-id="d557d-103">IoT Merkezi uygulamasını siler.</span><span class="sxs-lookup"><span data-stu-id="d557d-103">Deletes an IoT Central Application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d557d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d557d-104">SYNTAX</span></span>

### <span data-ttu-id="d557d-105">Resourceıdparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d557d-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzureRmIotCentralApp [-PassThru] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d557d-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="d557d-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d557d-107">Interactiveıotmerkezileştirme Parametrekümesi</span><span class="sxs-lookup"><span data-stu-id="d557d-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzureRmIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d557d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d557d-108">DESCRIPTION</span></span>
<span data-ttu-id="d557d-109">Var olan bir IoT Merkezi uygulamasını siler.</span><span class="sxs-lookup"><span data-stu-id="d557d-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="d557d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d557d-110">EXAMPLES</span></span>

### <span data-ttu-id="d557d-111">Örnek 1 Delete ve IoT Merkezi uygulaması</span><span class="sxs-lookup"><span data-stu-id="d557d-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="d557d-112">Sağlanan IoT Merkezi uygulamasını siler.</span><span class="sxs-lookup"><span data-stu-id="d557d-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="d557d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d557d-113">PARAMETERS</span></span>

### <span data-ttu-id="d557d-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="d557d-114">-AsJob</span></span>
<span data-ttu-id="d557d-115">Cmdlet 'i arka planda iş olarak çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="d557d-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="d557d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d557d-116">-DefaultProfile</span></span>
<span data-ttu-id="d557d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d557d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d557d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d557d-118">-InputObject</span></span>
<span data-ttu-id="d557d-119">IoT Merkezi uygulama giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d557d-119">Iot Central Application Input Object.</span></span>

```yaml
Type: PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d557d-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="d557d-120">-Name</span></span>
<span data-ttu-id="d557d-121">IoT Merkezi uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="d557d-121">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d557d-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d557d-122">-PassThru</span></span>
<span data-ttu-id="d557d-123">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="d557d-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d557d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d557d-124">-ResourceGroupName</span></span>
<span data-ttu-id="d557d-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d557d-125">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d557d-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d557d-126">-ResourceId</span></span>
<span data-ttu-id="d557d-127">IoT Merkezi uygulama kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="d557d-127">Iot Central Application Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d557d-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="d557d-128">-Confirm</span></span>
<span data-ttu-id="d557d-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d557d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d557d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d557d-130">-WhatIf</span></span>
<span data-ttu-id="d557d-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d557d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d557d-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d557d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d557d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d557d-133">CommonParameters</span></span>
<span data-ttu-id="d557d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d557d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d557d-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d557d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d557d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d557d-136">INPUTS</span></span>

### <span data-ttu-id="d557d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d557d-137">System.String</span></span>
### <span data-ttu-id="d557d-138">Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="d557d-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="d557d-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d557d-139">OUTPUTS</span></span>

### <span data-ttu-id="d557d-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d557d-140">System.Boolean</span></span>
## <span data-ttu-id="d557d-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d557d-141">NOTES</span></span>

## <span data-ttu-id="d557d-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d557d-142">RELATED LINKS</span></span>
