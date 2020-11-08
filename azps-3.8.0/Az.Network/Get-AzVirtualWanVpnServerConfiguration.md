---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: de25e096be96e54d2a8aa18f24bf9915a2f16538
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103546"
---
# <span data-ttu-id="65345-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="65345-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="65345-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65345-102">SYNOPSIS</span></span>
<span data-ttu-id="65345-103">Bu VirtualWan ile ilişkili tüm Vpnserveryapılandırmalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="65345-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="65345-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65345-104">SYNTAX</span></span>

### <span data-ttu-id="65345-105">ByVirtualWanName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="65345-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65345-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="65345-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65345-107">İ Virtualwanresourceıd</span><span class="sxs-lookup"><span data-stu-id="65345-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65345-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="65345-108">DESCRIPTION</span></span>
<span data-ttu-id="65345-109">**Get-AzVirtualWanVpnServerConfiguration** cmdlet 'i, bu virtualwan ile Ilişkili tüm Vpnserveryapılandırmalarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="65345-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="65345-110">Yani, bu Virtualswın Virutalhub 'ın altında herhangi bir P2SVpnGateways eklenmiş olan tüm VpnServerConfigurations.</span><span class="sxs-lookup"><span data-stu-id="65345-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="65345-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65345-111">EXAMPLES</span></span>

### <span data-ttu-id="65345-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="65345-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="65345-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65345-113">PARAMETERS</span></span>

### <span data-ttu-id="65345-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65345-114">-DefaultProfile</span></span>
<span data-ttu-id="65345-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="65345-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65345-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="65345-116">-Name</span></span>
<span data-ttu-id="65345-117">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="65345-117">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65345-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65345-118">-ResourceGroupName</span></span>
<span data-ttu-id="65345-119">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="65345-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65345-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="65345-120">-ResourceId</span></span>
<span data-ttu-id="65345-121">Sanal WAN için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="65345-121">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65345-122">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="65345-122">-VirtualWanObject</span></span>
<span data-ttu-id="65345-123">Sanal WAN nesnesi.</span><span class="sxs-lookup"><span data-stu-id="65345-123">The virtual wan object.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65345-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65345-124">CommonParameters</span></span>
<span data-ttu-id="65345-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65345-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65345-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65345-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65345-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65345-127">INPUTS</span></span>

### <span data-ttu-id="65345-128">System. String</span><span class="sxs-lookup"><span data-stu-id="65345-128">System.String</span></span>
<span data-ttu-id="65345-129">Microsoft. Azure. Commands. Network. model. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="65345-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="65345-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65345-130">OUTPUTS</span></span>

### <span data-ttu-id="65345-131">Microsoft. Azure. Commands. Network. model. PSVpnServerConfigurationsResponse</span><span class="sxs-lookup"><span data-stu-id="65345-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="65345-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65345-132">NOTES</span></span>

## <span data-ttu-id="65345-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65345-133">RELATED LINKS</span></span>
