---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B4102F33-979B-4649-99F4-96A295EAE43C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ddb0ac79f5164fb5c953dd1cf1efeff8391d30fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105465"
---
# <span data-ttu-id="123f8-101">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="123f8-101">Reset-AzureVNetGateway</span></span>

## <span data-ttu-id="123f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="123f8-102">SYNOPSIS</span></span>
<span data-ttu-id="123f8-103">Sanal ağ VPN ağ geçidini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="123f8-103">Resets a virtual network VPN gateway.</span></span>

## <span data-ttu-id="123f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="123f8-104">SYNTAX</span></span>

```
Reset-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="123f8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="123f8-105">DESCRIPTION</span></span>
<span data-ttu-id="123f8-106">**Reset-AzureVNetGateway** cmdlet 'i, sanal özel ağ (VPN) sanal ağ geçidini sıfırlar ve yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="123f8-106">The **Reset-AzureVNetGateway** cmdlet resets and restarts a virtual private network (VPN) virtual network gateway.</span></span>

## <span data-ttu-id="123f8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="123f8-107">EXAMPLES</span></span>

### <span data-ttu-id="123f8-108">Örnek 1: sanal ağ geçidini sıfırlama</span><span class="sxs-lookup"><span data-stu-id="123f8-108">Example 1: Reset a virtual network gateway</span></span>
```
PS C:\> Reset-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="123f8-109">Bu komut, ContosoVN07 adındaki sanal ağdan sanal ağ geçidini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="123f8-109">This command resets the virtual network gateway from the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="123f8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="123f8-110">PARAMETERS</span></span>

### <span data-ttu-id="123f8-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="123f8-111">-Profile</span></span>
<span data-ttu-id="123f8-112">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="123f8-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="123f8-113">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="123f8-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="123f8-114">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="123f8-114">-VNetName</span></span>
<span data-ttu-id="123f8-115">Bu cmdlet 'in sıfırkullandığı sanal ağ ağ geçidini içeren sanal ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="123f8-115">Specifies the virtual network that contains the virtual network gateway that this cmdlet resets.</span></span>

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

### <span data-ttu-id="123f8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="123f8-116">CommonParameters</span></span>
<span data-ttu-id="123f8-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="123f8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="123f8-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="123f8-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="123f8-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="123f8-119">INPUTS</span></span>

## <span data-ttu-id="123f8-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="123f8-120">OUTPUTS</span></span>

## <span data-ttu-id="123f8-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="123f8-121">NOTES</span></span>

## <span data-ttu-id="123f8-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="123f8-122">RELATED LINKS</span></span>

[<span data-ttu-id="123f8-123">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="123f8-123">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="123f8-124">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="123f8-124">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="123f8-125">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="123f8-125">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="123f8-126">Resize-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="123f8-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="123f8-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="123f8-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


