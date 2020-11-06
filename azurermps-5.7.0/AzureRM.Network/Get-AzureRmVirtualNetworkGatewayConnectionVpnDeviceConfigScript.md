---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 3fb557f29203971d54674f0f18476e249644eeb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594923"
---
# <span data-ttu-id="fc014-101">Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="fc014-101">Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="fc014-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc014-102">SYNOPSIS</span></span>
<span data-ttu-id="fc014-103">Bu komut, bağlantı kaynağını, VPN cihazı markasına, modeli, bellenim sürümünü alır ve müşterilerin Şirket içi VPN aygıtlarına doğrudan uygulayacakları ilgili yapılandırma betiğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="fc014-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="fc014-104">Komut dosyası seçili aygıtın söz dizimini alır ve Azure ağ geçidi genel IP adresleri, sanal ağ adresi önekleri, VPN tüneli önceden paylaşılan anahtarı vb. gibi gerekli parametreleri doldurur</span><span class="sxs-lookup"><span data-stu-id="fc014-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc014-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc014-105">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc014-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc014-106">DESCRIPTION</span></span>
<span data-ttu-id="fc014-107">Bu komut, bağlantı kaynağını, VPN cihazı markasına, modeli, bellenim sürümünü alır ve müşterilerin Şirket içi VPN aygıtlarına doğrudan uygulayacakları ilgili yapılandırma betiğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="fc014-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="fc014-108">Komut dosyası seçili aygıtın söz dizimini alır ve Azure ağ geçidi genel IP adresleri, sanal ağ adresi önekleri, VPN tüneli önceden paylaşılan anahtarı vb. gibi gerekli parametreleri doldurur</span><span class="sxs-lookup"><span data-stu-id="fc014-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="fc014-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc014-109">EXAMPLES</span></span>

### <span data-ttu-id="fc014-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fc014-110">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="fc014-111">Yukarıdaki örnekte, desteklenen VPN cihaz markalarının, modellerin ve bellenim sürümlerinin alınması için Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fc014-111">The above example uses Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="fc014-112">Daha sonra VirtualNetworkGatewayConnection "TestConnection" için bir VPN cihaz yapılandırması oluşturmak için döndürülen model bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="fc014-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="fc014-113">Bu örnekte kullanılan cihazda DeviceFamily "IOS-test", Devicevenun "Cisco-test" ve FirmwareVersion 20 bulunur.</span><span class="sxs-lookup"><span data-stu-id="fc014-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="fc014-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc014-114">PARAMETERS</span></span>

### <span data-ttu-id="fc014-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc014-115">-DefaultProfile</span></span>
<span data-ttu-id="fc014-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fc014-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc014-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="fc014-117">-DeviceFamily</span></span>
<span data-ttu-id="fc014-118">VPN cihaz modelinin/ailesinin adı.</span><span class="sxs-lookup"><span data-stu-id="fc014-118">Name of the VPN device model/family.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc014-119">-Devicevençi</span><span class="sxs-lookup"><span data-stu-id="fc014-119">-DeviceVendor</span></span>
<span data-ttu-id="fc014-120">VPN cihazı üreticisinin adı.</span><span class="sxs-lookup"><span data-stu-id="fc014-120">Name of the VPN device vendor.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc014-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="fc014-121">-FirmwareVersion</span></span>
<span data-ttu-id="fc014-122">VPN aygıtının bellenim sürümü.</span><span class="sxs-lookup"><span data-stu-id="fc014-122">Firmware version of the VPN device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc014-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="fc014-123">-Name</span></span>
<span data-ttu-id="fc014-124">Yapılandırma oluşturulacak bağlantının kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="fc014-124">The resource name of the connection for which the configuration is to be generated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc014-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc014-125">-ResourceGroupName</span></span>
<span data-ttu-id="fc014-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="fc014-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc014-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="fc014-127">-Confirm</span></span>
<span data-ttu-id="fc014-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fc014-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc014-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc014-129">-WhatIf</span></span>
<span data-ttu-id="fc014-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fc014-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc014-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fc014-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc014-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc014-132">CommonParameters</span></span>
<span data-ttu-id="fc014-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc014-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc014-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc014-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc014-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc014-135">INPUTS</span></span>

### <span data-ttu-id="fc014-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fc014-136">System.String</span></span>

## <span data-ttu-id="fc014-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc014-137">OUTPUTS</span></span>

### <span data-ttu-id="fc014-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fc014-138">System.String</span></span>

## <span data-ttu-id="fc014-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc014-139">NOTES</span></span>

## <span data-ttu-id="fc014-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc014-140">RELATED LINKS</span></span>

