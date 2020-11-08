---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4024D20D-46DF-4ED8-A091-E6E17F840E40
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92c6ba8827906fbfc51b121e4500dea3ec4555d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106279"
---
# <span data-ttu-id="47723-101">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="47723-101">Get-AzureVNetGateway</span></span>

## <span data-ttu-id="47723-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47723-102">SYNOPSIS</span></span>
<span data-ttu-id="47723-103">Sanal ağ geçidinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="47723-103">Gets the status of a virtual network gateway.</span></span>

## <span data-ttu-id="47723-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47723-104">SYNTAX</span></span>

```
Get-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="47723-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="47723-105">DESCRIPTION</span></span>
<span data-ttu-id="47723-106">**Get-AzureVNetGateway** cmdlet 'i var olan bir sanal ağ ağ geçidinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="47723-106">The **Get-AzureVNetGateway** cmdlet gets the status of an existing virtual network gateway.</span></span>

## <span data-ttu-id="47723-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47723-107">EXAMPLES</span></span>

### <span data-ttu-id="47723-108">Örnek 1: sanal ağ geçidinin durumunu alma</span><span class="sxs-lookup"><span data-stu-id="47723-108">Example 1: Get the status of a virtual network gateway</span></span>
```
PS C:\> Get-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="47723-109">Bu komut, ContosoVN07 adındaki sanal ağ için sanal ağ geçidinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="47723-109">This command gets that status of the virtual network gateway for the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="47723-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47723-110">PARAMETERS</span></span>

### <span data-ttu-id="47723-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="47723-111">-Profile</span></span>
<span data-ttu-id="47723-112">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="47723-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="47723-113">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="47723-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="47723-114">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="47723-114">-VNetName</span></span>
<span data-ttu-id="47723-115">Bu cmdlet 'in durumu aldığı sanal ağ ağ geçidini içeren sanal ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="47723-115">Specifies the virtual network that contains the virtual network gateway for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="47723-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47723-116">CommonParameters</span></span>
<span data-ttu-id="47723-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47723-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47723-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47723-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47723-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47723-119">INPUTS</span></span>

## <span data-ttu-id="47723-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47723-120">OUTPUTS</span></span>

## <span data-ttu-id="47723-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47723-121">NOTES</span></span>

## <span data-ttu-id="47723-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47723-122">RELATED LINKS</span></span>

[<span data-ttu-id="47723-123">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="47723-123">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="47723-124">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="47723-124">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="47723-125">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="47723-125">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="47723-126">Resize-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="47723-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="47723-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="47723-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


