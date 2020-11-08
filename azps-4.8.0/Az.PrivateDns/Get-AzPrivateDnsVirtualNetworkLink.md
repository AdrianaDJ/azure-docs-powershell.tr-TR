---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 60da913ea7743be288e58eee9e4840c15e4818b4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268392"
---
# <span data-ttu-id="7f09a-101">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="7f09a-101">Get-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="7f09a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f09a-102">SYNOPSIS</span></span>
<span data-ttu-id="7f09a-103">Belirtilen özel DNS bölgesiyle ilişkili sanal ağ bağlantısını alır.</span><span class="sxs-lookup"><span data-stu-id="7f09a-103">Gets a virtual network link associated with the specified Private DNS zone.</span></span>

## <span data-ttu-id="7f09a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f09a-104">SYNTAX</span></span>

```
Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f09a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f09a-105">DESCRIPTION</span></span>
<span data-ttu-id="7f09a-106">**Get-AzPrivateDnsVirtualNetworkLink** cmdlet 'i belirtilen kaynak grubundan belirli BIR özel DNS bölgesiyle ilişkilendirilmiş sanal ağ bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="7f09a-106">The **Get-AzPrivateDnsVirtualNetworkLink** cmdlet gets virtual network links associated with a particular Private DNS zone from the specified resource group.</span></span>
<span data-ttu-id="7f09a-107">*Name* parametresini belirtirseniz, tek bir **Psprivatednsvirtualnetworklink** nesnesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="7f09a-107">If you specify the *Name* parameter, a single **PSPrivateDnsVirtualNetworkLink** object is returned.</span></span>
<span data-ttu-id="7f09a-108">*Name* parametresini belirtmezseniz, belirtilen kaynak grubundaki Bölgeyle ilişkili tüm bağlantıları içeren bir dizi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="7f09a-108">If you do not specify the *Name* parameter, an array containing all of the links associated with the zone in the specified resource group is returned.</span></span>
<span data-ttu-id="7f09a-109">Bağlantıyı güncelleştirmek için **Psprivatednsvirtualnetworklink** nesnesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7f09a-109">You can use the **PSPrivateDnsVirtualNetworkLink** object to update the link.</span></span>

## <span data-ttu-id="7f09a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f09a-110">EXAMPLES</span></span>

### <span data-ttu-id="7f09a-111">Örnek 1: sanal ağ bağlantısı edinin.</span><span class="sxs-lookup"><span data-stu-id="7f09a-111">Example 1: Get a virtual network link.</span></span>
```
PS C:\> $Link = Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"

The link object returned looks like the following:

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="7f09a-112">Bu örnekte, myzone.com adlı özel DNS bölgesiyle ilişkili sanal ağ bağlantısı, belirtilen kaynak grubundan alınır ve $Link değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="7f09a-112">This example gets the virtual network link mylink associated with the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Link variable.</span></span>

### <span data-ttu-id="7f09a-113">Örnek 2: kaynak grubundaki bir bölgeyle ilişkili tüm bağlantıları edinin.</span><span class="sxs-lookup"><span data-stu-id="7f09a-113">Example 2: Get all of the links associated with a zone in a resource group.</span></span>
```
PS C:\> $Links = Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"

Name                    : mylink1
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink1
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded

Name                    : mylink2
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink2
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="7f09a-114">Bu örnekte, belirtilen kaynak grubundaki özel DNS bölgesi "myzone.com" ile ilişkili sanal ağ bağlantılarının tümü alınır ve $Links değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="7f09a-114">This example gets all of the virtual network links associated with the Private DNS zone "myzone.com" in the specified resource group, and then stores it in the $Links variable.</span></span>

## <span data-ttu-id="7f09a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f09a-115">PARAMETERS</span></span>

### <span data-ttu-id="7f09a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f09a-116">-DefaultProfile</span></span>
<span data-ttu-id="7f09a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7f09a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f09a-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="7f09a-118">-Name</span></span>
<span data-ttu-id="7f09a-119">Alınacak sanal ağ bağlantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f09a-119">Specifies the name of the virtual network link to get.</span></span>
<span data-ttu-id="7f09a-120">*Ad* parametresi için bir değer belirtmezseniz, bu cmdlet belirtilen kaynak grubundaki BELIRTILEN özel DNS bölgesiyle ilişkili tüm bağlantıları alır.</span><span class="sxs-lookup"><span data-stu-id="7f09a-120">If you do not specify a value for the *Name* parameter, this cmdlet gets all links associated with the specified Private DNS zone in the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f09a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f09a-121">-ResourceGroupName</span></span>
<span data-ttu-id="7f09a-122">Alınacak sanal ağ bağlantısını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f09a-122">Specifies the name of the resource group that contains the virtual network link to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f09a-123">-BölgeAdı</span><span class="sxs-lookup"><span data-stu-id="7f09a-123">-ZoneName</span></span>
<span data-ttu-id="7f09a-124">Sanal ağ bağlantısının bağlandığı özel DNS bölgesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f09a-124">Specifies the name of the Private DNS zone that the virtual network link is linked to.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f09a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f09a-125">CommonParameters</span></span>
<span data-ttu-id="7f09a-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f09a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f09a-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f09a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f09a-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f09a-128">INPUTS</span></span>

### <span data-ttu-id="7f09a-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7f09a-129">None</span></span>

## <span data-ttu-id="7f09a-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f09a-130">OUTPUTS</span></span>

### <span data-ttu-id="7f09a-131">Microsoft. Azure. Commands. PrivateDns. model. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="7f09a-131">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="7f09a-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f09a-132">NOTES</span></span>

## <span data-ttu-id="7f09a-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f09a-133">RELATED LINKS</span></span>

[<span data-ttu-id="7f09a-134">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="7f09a-134">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="7f09a-135">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="7f09a-135">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="7f09a-136">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="7f09a-136">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
