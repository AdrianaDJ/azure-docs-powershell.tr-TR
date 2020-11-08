---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DF95285F-97F4-4064-8E27-EE6E93843E55
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0a14865c986bf6439df833a38f87835792a6e3c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105626"
---
# <span data-ttu-id="b793c-101">Get-AzureRemoteAppVpnDevice</span><span class="sxs-lookup"><span data-stu-id="b793c-101">Get-AzureRemoteAppVpnDevice</span></span>

## <span data-ttu-id="b793c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b793c-102">SYNOPSIS</span></span>
<span data-ttu-id="b793c-103">VPN cihazı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="b793c-103">Retrieves information about a VPN device.</span></span>

## <span data-ttu-id="b793c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b793c-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVpnDevice [-VNetName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b793c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b793c-105">DESCRIPTION</span></span>
<span data-ttu-id="b793c-106">**Get-AzureRemoteAppVpnDevice** cmdlet 'i sanal özel ağ (VPN) cihazı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="b793c-106">The **Get-AzureRemoteAppVpnDevice** cmdlet retrieves information about a virtual private network (VPN) device.</span></span>

## <span data-ttu-id="b793c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b793c-107">EXAMPLES</span></span>

### <span data-ttu-id="b793c-108">Örnek 1: sanal ağ için kullanılabilir VPN cihaz yapılandırmalarını döndürme</span><span class="sxs-lookup"><span data-stu-id="b793c-108">Example 1: Return the available VPN device configurations for a virtual network</span></span>
```
PS C:\> Get-AzureRemoteVpnDevice -VNetName "ContosoVNet"


Name                   Platforms

----                   ---------

Cisco Systems, Inc.    {ASA 5500 Series Adaptive Security Appliances, ASR 1000 Series Aggregation Services Routers, ASR 1000 Series Aggregation Services Routers - Dynamic Routing, ISR Series Integrated Services Routers...} 

Juniper Networks, Inc. {SRX Series Routers, SRX Series Routers - Dynamic Routing, J Series Routers, J Series Routers - Dynamic Routing...} 

Microsoft Corporation  {RRAS}
```

<span data-ttu-id="b793c-109">Bu komut, belirtilen sanal ağın kullanılabilir VPN cihaz yapılandırmalarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="b793c-109">This command returns the available VPN device configurations for the specified virtual network.</span></span>

## <span data-ttu-id="b793c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b793c-110">PARAMETERS</span></span>

### <span data-ttu-id="b793c-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="b793c-111">-Profile</span></span>
<span data-ttu-id="b793c-112">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b793c-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b793c-113">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b793c-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b793c-114">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="b793c-114">-VNetName</span></span>
<span data-ttu-id="b793c-115">Azure RemoteApp sanal ağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b793c-115">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b793c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b793c-116">CommonParameters</span></span>
<span data-ttu-id="b793c-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b793c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b793c-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b793c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b793c-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b793c-119">INPUTS</span></span>

## <span data-ttu-id="b793c-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b793c-120">OUTPUTS</span></span>

### <span data-ttu-id="b793c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b793c-121">System.String</span></span>

## <span data-ttu-id="b793c-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b793c-122">NOTES</span></span>

## <span data-ttu-id="b793c-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b793c-123">RELATED LINKS</span></span>

[<span data-ttu-id="b793c-124">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="b793c-124">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="b793c-125">Get-Azureremoteappvpndeviceconfigscrıpt</span><span class="sxs-lookup"><span data-stu-id="b793c-125">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>](./Get-AzureRemoteAppVpnDeviceConfigScript.md)


