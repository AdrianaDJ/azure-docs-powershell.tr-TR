---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 70899AAC-BF64-4FFA-9DAF-92E859D0B271
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3b30172f947c1c8bf39a8be84039d9166d6ea290
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106414"
---
# <span data-ttu-id="d2467-101">Set-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="d2467-101">Set-AzureVNetGateway</span></span>

## <span data-ttu-id="d2467-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2467-102">SYNOPSIS</span></span>
<span data-ttu-id="d2467-103">Bir Azure sanal ağı için VPN ağ geçidini etkinleştirilir veya devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="d2467-103">Enables or disables a VPN gateway for an Azure virtual network.</span></span>

## <span data-ttu-id="d2467-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2467-104">SYNTAX</span></span>

### <span data-ttu-id="d2467-105">Bağlan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d2467-105">Connect (Default)</span></span>
```
Set-AzureVNetGateway [-Connect] -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2467-106">Bilgisayarla</span><span class="sxs-lookup"><span data-stu-id="d2467-106">Disconnect</span></span>
```
Set-AzureVNetGateway [-Disconnect] -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d2467-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2467-107">DESCRIPTION</span></span>
<span data-ttu-id="d2467-108">**Set-AzureVNetGateway** cmdlet 'ı, Azure sanal ağı için sanal özel ağ (VPN) ağ geçidini devre dışı bırakır veya devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="d2467-108">The **Set-AzureVNetGateway** cmdlet enables or disables a virtual private network (VPN) gateway for an Azure virtual network.</span></span>
<span data-ttu-id="d2467-109">Sanal ağ geçidi sanal ağa bağlanmak için VPN uç noktasıdır.</span><span class="sxs-lookup"><span data-stu-id="d2467-109">A virtual network gateway is a VPN endpoint for connecting to a virtual network.</span></span>
<span data-ttu-id="d2467-110">Şirket içi yerel ağ sitesi ile sanal ağ arasındaki VPN bağlantısını etkinleştirmek veya devre dışı bırakmak için, *Bağlan* veya *Bağlantıyı kapat* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="d2467-110">Specify the *Connect* or *Disconnect* parameter to enable or disable the VPN connection between an on-premises local network site and a virtual network.</span></span>

## <span data-ttu-id="d2467-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2467-111">EXAMPLES</span></span>

### <span data-ttu-id="d2467-112">Örnek 1: sanal ağ için sanal ağ geçidini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="d2467-112">Example 1: Enable a virtual network gateway for a virtual network</span></span>
```
PS C:\> Set-AzureVNetGateway -Connect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

<span data-ttu-id="d2467-113">Bu komut, ContosoProdNet adlı Azure sanal ağı ile ContosoBranchOffice adlı yerel ağ sitesinin VPN cihazı arasındaki sanal ağ ağ geçidini etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="d2467-113">This command enables the virtual network gateway between the Azure virtual network named ContosoProdNet and the VPN device for the local network site named ContosoBranchOffice.</span></span>

### <span data-ttu-id="d2467-114">Örnek 2: sanal ağ için sanal ağ geçidini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="d2467-114">Example 2: Disable a virtual network gateway for a virtual network</span></span>
```
PS C:\> Set-AzureVNetGateway -Disconnect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

<span data-ttu-id="d2467-115">Bu komut, ContosoProdNet adlı Azure sanal ağı ile ContosoBranchOffice adlı yerel ağ sitesinin VPN cihazı arasındaki sanal ağ ağ geçidini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="d2467-115">This command disables the virtual network gateway between the Azure virtual network named ContosoProdNet and the VPN device for the local network site named ContosoBranchOffice.</span></span>

## <span data-ttu-id="d2467-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2467-116">PARAMETERS</span></span>

### <span data-ttu-id="d2467-117">-Bağlantı</span><span class="sxs-lookup"><span data-stu-id="d2467-117">-Connect</span></span>
<span data-ttu-id="d2467-118">Bu cmdlet 'in sanal ağ ile yerel ağ sitesi arasındaki VPN bağlantısını etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="d2467-118">Indicates that this cmdlet enables the VPN connection between a virtual network and a local network site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Connect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2467-119">-Bağlantısındaki</span><span class="sxs-lookup"><span data-stu-id="d2467-119">-Disconnect</span></span>
<span data-ttu-id="d2467-120">Bu cmdlet 'in sanal ağ ile yerel ağ sitesi arasındaki VPN bağlantısını devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d2467-120">Indicates that this cmdlet disables the VPN connection between a virtual network and a local network site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disconnect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2467-121">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="d2467-121">-LocalNetworkSiteName</span></span>
<span data-ttu-id="d2467-122">Bu cmdlet 'in VPN bağlantısını etkinleştirmesine veya devre dışı bırakabildiği şirket içi yerel ağ sitesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2467-122">Specifies the name of the on-premises local network site for which this cmdlet enables or disables the VPN connection.</span></span>

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

### <span data-ttu-id="d2467-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="d2467-123">-Profile</span></span>
<span data-ttu-id="d2467-124">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2467-124">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d2467-125">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="d2467-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d2467-126">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="d2467-126">-VNetName</span></span>
<span data-ttu-id="d2467-127">Bu cmdlet 'in VPN bağlantısını etkinleştirmesine veya devre dışı bırakacağını belirten sanal ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2467-127">Specifies the virtual network for which this cmdlet enables or disables the VPN connection.</span></span>

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

### <span data-ttu-id="d2467-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2467-128">CommonParameters</span></span>
<span data-ttu-id="d2467-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2467-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2467-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2467-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2467-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2467-131">INPUTS</span></span>

## <span data-ttu-id="d2467-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2467-132">OUTPUTS</span></span>

## <span data-ttu-id="d2467-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2467-133">NOTES</span></span>

## <span data-ttu-id="d2467-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2467-134">RELATED LINKS</span></span>

[<span data-ttu-id="d2467-135">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="d2467-135">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="d2467-136">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="d2467-136">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="d2467-137">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="d2467-137">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="d2467-138">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="d2467-138">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="d2467-139">Resize-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="d2467-139">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)


