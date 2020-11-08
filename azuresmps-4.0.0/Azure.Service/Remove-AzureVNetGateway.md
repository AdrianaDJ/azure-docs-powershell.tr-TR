---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E6EF9B8-9709-4E59-A1E5-78CDA4EAAE1B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88dcd2f4bad149396d58948d3d656defdf055104
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105490"
---
# <span data-ttu-id="fe246-101">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="fe246-101">Remove-AzureVNetGateway</span></span>

## <span data-ttu-id="fe246-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe246-102">SYNOPSIS</span></span>
<span data-ttu-id="fe246-103">VPN ağ geçidini siler.</span><span class="sxs-lookup"><span data-stu-id="fe246-103">Deletes a VPN gateway.</span></span>

## <span data-ttu-id="fe246-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fe246-104">SYNTAX</span></span>

```
Remove-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fe246-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe246-105">DESCRIPTION</span></span>
<span data-ttu-id="fe246-106">**Remove-AzureVNetGateway** cmdlet 'i sanal ağ için var olan bir sanal özel ağ (VPN) ağ geçidini siler.</span><span class="sxs-lookup"><span data-stu-id="fe246-106">The **Remove-AzureVNetGateway** cmdlet deletes an existing virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="fe246-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fe246-107">EXAMPLES</span></span>

### <span data-ttu-id="fe246-108">Örnek 1: sanal ağ geçidini kaldırma</span><span class="sxs-lookup"><span data-stu-id="fe246-108">Example 1: Remove a virtual network gateway</span></span>
```
PS C:\> Remove-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="fe246-109">Bu komut, ContosoVN07 adındaki sanal ağdan sanal ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fe246-109">This command removes the virtual network gateway from the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="fe246-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fe246-110">PARAMETERS</span></span>

### <span data-ttu-id="fe246-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="fe246-111">-Profile</span></span>
<span data-ttu-id="fe246-112">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe246-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="fe246-113">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="fe246-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe246-114">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="fe246-114">-VNetName</span></span>
<span data-ttu-id="fe246-115">Bu cmdlet 'in VPN ağ geçidini sildiği sanal ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe246-115">Specifies the virtual network in which this cmdlet deletes the VPN gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe246-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe246-116">CommonParameters</span></span>
<span data-ttu-id="fe246-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fe246-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe246-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe246-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe246-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fe246-119">INPUTS</span></span>

## <span data-ttu-id="fe246-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fe246-120">OUTPUTS</span></span>

## <span data-ttu-id="fe246-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fe246-121">NOTES</span></span>

## <span data-ttu-id="fe246-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fe246-122">RELATED LINKS</span></span>

[<span data-ttu-id="fe246-123">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="fe246-123">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="fe246-124">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="fe246-124">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="fe246-125">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="fe246-125">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="fe246-126">Resize-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="fe246-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="fe246-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="fe246-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


