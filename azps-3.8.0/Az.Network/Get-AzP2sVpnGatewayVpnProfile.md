---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
ms.openlocfilehash: 60937898e7e8c0532a0f0815ee44f2e9f75041c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098787"
---
# <span data-ttu-id="49637-101">Get-AzP2sVpnGatewayVpnProfile</span><span class="sxs-lookup"><span data-stu-id="49637-101">Get-AzP2sVpnGatewayVpnProfile</span></span>

## <span data-ttu-id="49637-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49637-102">SYNOPSIS</span></span>
<span data-ttu-id="49637-103">Site istemcisi kurulumunu P2SVpnGateway için site bağlantısı noktası olacak şekilde ayarlamak için, müşterinin SAS URL 'sini oluşturur ve döndürür.</span><span class="sxs-lookup"><span data-stu-id="49637-103">Generates and returns a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span>

## <span data-ttu-id="49637-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49637-104">SYNTAX</span></span>

### <span data-ttu-id="49637-105">ByP2SVpnGatewayName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="49637-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayVpnProfile [-Name <String>] -ResourceGroupName <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49637-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="49637-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -InputObject <PSP2SVpnGateway> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49637-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="49637-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -ResourceId <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49637-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="49637-108">DESCRIPTION</span></span>
<span data-ttu-id="49637-109">**Get-AzP2sVpnGatewayVpnProfile** cmdlet 'i, müşteri IÇIN bir SAS URL 'si oluşturup almanızı ve site istemcisi kurulumunu, P2SVpnGateway için site bağlantısını göstermesi için</span><span class="sxs-lookup"><span data-stu-id="49637-109">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="49637-110">Bu VPN profilini kullanarak site istemcisi kurulumu</span><span class="sxs-lookup"><span data-stu-id="49637-110">Point to site client setup using this Vpn profile can connect to this specific P2SVpnGateway only.</span></span>

## <span data-ttu-id="49637-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49637-111">EXAMPLES</span></span>

### <span data-ttu-id="49637-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="49637-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayVpnProfile -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -AuthenticationMethod EAPTLS


ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/8cf00031-37ec-4949-b74a-48f9021bf4c0/vpnprofile/2f132439-1051-44c6-9128-b704c1c48cf7/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=HmBSprVrs
             6hDY3x1HX958nimOjavnEjL2rlSuKIIW8Q%3D&st=2019-10-25T19%3A20%3A04Z&se=2019-10-25T20%3A20%3A04Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="49637-113">**Get-AzP2sVpnGatewayVpnProfile** cmdlet 'i, müşteri IÇIN bir SAS URL 'si oluşturup almanızı ve site istemcisi kurulumunu, P2SVpnGateway için site bağlantısını göstermesi için</span><span class="sxs-lookup"><span data-stu-id="49637-113">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="49637-114">ProfileUrl, müşterinin site istemcisi kurulumu üzerine gelmek için VPN profilini indirebileceği SAS URL 'sini gösterir.</span><span class="sxs-lookup"><span data-stu-id="49637-114">ProfileUrl shows the SAS url from where customer can download Vpn profile for point to site client setup.</span></span>

## <span data-ttu-id="49637-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49637-115">PARAMETERS</span></span>

### <span data-ttu-id="49637-116">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="49637-116">-AuthenticationMethod</span></span>
<span data-ttu-id="49637-117">Kimlik doğrulama yöntemi</span><span class="sxs-lookup"><span data-stu-id="49637-117">Authentication Method</span></span>

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

### <span data-ttu-id="49637-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49637-118">-DefaultProfile</span></span>
<span data-ttu-id="49637-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="49637-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49637-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49637-120">-InputObject</span></span>
<span data-ttu-id="49637-121">Değiştirilecek P2S VPN ağ geçidi nesnesi</span><span class="sxs-lookup"><span data-stu-id="49637-121">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49637-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="49637-122">-Name</span></span>
<span data-ttu-id="49637-123">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="49637-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49637-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49637-124">-ResourceGroupName</span></span>
<span data-ttu-id="49637-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="49637-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49637-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="49637-126">-ResourceId</span></span>
<span data-ttu-id="49637-127">Değiştirilecek P2SVpnGateway Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="49637-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49637-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49637-128">CommonParameters</span></span>
<span data-ttu-id="49637-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="49637-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49637-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49637-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49637-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49637-131">INPUTS</span></span>

### <span data-ttu-id="49637-132">System. String</span><span class="sxs-lookup"><span data-stu-id="49637-132">System.String</span></span>
<span data-ttu-id="49637-133">Microsoft. Azure. Commands. Network. modeller. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="49637-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="49637-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49637-134">OUTPUTS</span></span>

### <span data-ttu-id="49637-135">Microsoft. Azure. Commands. Network. model. Psvpnprofileresß</span><span class="sxs-lookup"><span data-stu-id="49637-135">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="49637-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49637-136">NOTES</span></span>

## <span data-ttu-id="49637-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49637-137">RELATED LINKS</span></span>