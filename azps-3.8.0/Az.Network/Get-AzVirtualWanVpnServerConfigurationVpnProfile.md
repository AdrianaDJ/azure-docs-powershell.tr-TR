---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfigurationvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
ms.openlocfilehash: 5e19f63c0497535c44513c55a28d7117d0783574
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938074"
---
# <span data-ttu-id="bf0c2-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span><span class="sxs-lookup"><span data-stu-id="bf0c2-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span></span>

## <span data-ttu-id="bf0c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf0c2-102">SYNOPSIS</span></span>
<span data-ttu-id="bf0c2-103">Site istemcisi kurulumu 'nun noktası için VirtualWan-VpnServerConfiguration düzeyinde VPN profili oluşturur ve indirir.</span><span class="sxs-lookup"><span data-stu-id="bf0c2-103">Generates and downloads Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="bf0c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf0c2-104">SYNTAX</span></span>

### <span data-ttu-id="bf0c2-105">ByVirtualWanNameByVpnServerConfigurationObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bf0c2-105">ByVirtualWanNameByVpnServerConfigurationObject (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf0c2-106">Byvirtualwannamebyvpnserverconfigurationresourceıd</span><span class="sxs-lookup"><span data-stu-id="bf0c2-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bf0c2-107">ByVirtualWanObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="bf0c2-107">ByVirtualWanObjectByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf0c2-108">Byvirtualwanobjectbyvpnserverconfigurationresourceıd</span><span class="sxs-lookup"><span data-stu-id="bf0c2-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bf0c2-109">Byvirtualwanresourceıdbyvpnserverconfigurationobject</span><span class="sxs-lookup"><span data-stu-id="bf0c2-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf0c2-110">Byvirtualwanresourceıdbyvpnserverconfigurationresourceıd</span><span class="sxs-lookup"><span data-stu-id="bf0c2-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String> -VpnServerConfigurationId <String>
 [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf0c2-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf0c2-111">DESCRIPTION</span></span>
<span data-ttu-id="bf0c2-112">**Get-AzVirtualWanVpnServerConfigurationVpnProfile** cmdlet 'i, site istemcisi kurulumu için VirtualWan-VpnServerConfiguration düzeyinde VPN profili oluşturup yüklemenize imkan verir.</span><span class="sxs-lookup"><span data-stu-id="bf0c2-112">The **Get-AzVirtualWanVpnServerConfigurationVpnProfile** cmdlet enables you to generate and download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span> <span data-ttu-id="bf0c2-113">Bu, site istemcisinin Azure P2SVpnGateway 'e noktadan itibaren site bağlantısı noktası için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="bf0c2-113">This is required for Point to site connectivity from Point to site client to Azure P2SVpnGateway.</span></span>

## <span data-ttu-id="bf0c2-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf0c2-114">EXAMPLES</span></span>

### <span data-ttu-id="bf0c2-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bf0c2-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfigurationVpnProfile -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting -VpnServerConfiguration $vpnServerConfig -AuthenticationMethod EAPTLS

ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/aa316f33-d0f6-4e61-994a-9aa24c0e5f70/vpnprofile/eb99aa3d-1106-49eb-9644-791c045c5cca/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=kZinevNqW
             qsEAbWAcYiKfUHFxZzh2hwvtb49dfVtUDA%3D&st=2019-10-25T19%3A52%3A36Z&se=2019-10-25T20%3A52%3A36Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="bf0c2-116">Yukarıdaki komut, VirtualWan-VpnServerConfiguration müşteri için SAS URL 'Sini oluşturur ve bu müşteri için</span><span class="sxs-lookup"><span data-stu-id="bf0c2-116">The above command will generate and returns SAS Url for customer to download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="bf0c2-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf0c2-117">PARAMETERS</span></span>

### <span data-ttu-id="bf0c2-118">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="bf0c2-118">-AuthenticationMethod</span></span>
<span data-ttu-id="bf0c2-119">Kimlik doğrulama yöntemi</span><span class="sxs-lookup"><span data-stu-id="bf0c2-119">Authentication Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0c2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf0c2-120">-DefaultProfile</span></span>
<span data-ttu-id="bf0c2-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bf0c2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf0c2-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="bf0c2-122">-Name</span></span>
<span data-ttu-id="bf0c2-123">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="bf0c2-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanNameByVpnServerConfigurationResourceId
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0c2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf0c2-124">-ResourceGroupName</span></span>
<span data-ttu-id="bf0c2-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="bf0c2-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0c2-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bf0c2-126">-ResourceId</span></span>
<span data-ttu-id="bf0c2-127">Sanal WAN için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="bf0c2-127">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceIdByVpnServerConfigurationObject, ByVirtualWanResourceIdByVpnServerConfigurationResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf0c2-128">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="bf0c2-128">-VirtualWanObject</span></span>
<span data-ttu-id="bf0c2-129">Sanal WAN nesnesi.</span><span class="sxs-lookup"><span data-stu-id="bf0c2-129">The virtual wan object.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnServerConfigurationObject, ByVirtualWanObjectByVpnServerConfigurationResourceId
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf0c2-130">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf0c2-130">-VpnServerConfiguration</span></span>
<span data-ttu-id="bf0c2-131">Bu Virtualswın ilişkilendirildiği VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="bf0c2-131">The VpnServerConfiguration with which this VirtualWan is associated.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanObjectByVpnServerConfigurationObject, ByVirtualWanResourceIdByVpnServerConfigurationObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf0c2-132">-Vpnserverconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="bf0c2-132">-VpnServerConfigurationId</span></span>
<span data-ttu-id="bf0c2-133">VPN sunucunuzun kimliği bu sanal WAN ile ilişkilendirilecek.</span><span class="sxs-lookup"><span data-stu-id="bf0c2-133">The id of Vpn server configuraiton object this Virtual wan will be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationResourceId, ByVirtualWanObjectByVpnServerConfigurationResourceId, ByVirtualWanResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf0c2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf0c2-134">CommonParameters</span></span>
<span data-ttu-id="bf0c2-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf0c2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf0c2-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf0c2-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf0c2-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf0c2-137">INPUTS</span></span>

### <span data-ttu-id="bf0c2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="bf0c2-138">System.String</span></span>
<span data-ttu-id="bf0c2-139">Microsoft. Azure. Commands. Network. model. PSVirtualWan Microsoft. Azure. Commands. Network. model. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf0c2-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="bf0c2-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf0c2-140">OUTPUTS</span></span>

### <span data-ttu-id="bf0c2-141">Microsoft. Azure. Commands. Network. model. Psvpnprofileresß</span><span class="sxs-lookup"><span data-stu-id="bf0c2-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="bf0c2-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf0c2-142">NOTES</span></span>

## <span data-ttu-id="bf0c2-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf0c2-143">RELATED LINKS</span></span>