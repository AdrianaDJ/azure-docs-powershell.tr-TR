---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
ms.openlocfilehash: 0565956d7f40a633bc1aa2c2049ef9a7d764d77e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939706"
---
# <span data-ttu-id="02a5b-101">Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="02a5b-101">Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="02a5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02a5b-102">SYNOPSIS</span></span>
<span data-ttu-id="02a5b-103">Bu komut, bağlantı kaynağını, VPN cihazı markasına, modeli, bellenim sürümünü alır ve müşterilerin Şirket içi VPN aygıtlarına doğrudan uygulayacakları ilgili yapılandırma betiğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="02a5b-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="02a5b-104">Komut dosyası seçili aygıtın söz dizimini alır ve Azure ağ geçidi genel IP adresleri, sanal ağ adresi önekleri, VPN tüneli önceden paylaşılan anahtarı vb. gibi gerekli parametreleri doldurur</span><span class="sxs-lookup"><span data-stu-id="02a5b-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02a5b-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02a5b-105">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02a5b-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="02a5b-106">DESCRIPTION</span></span>
<span data-ttu-id="02a5b-107">Bu komut, bağlantı kaynağını, VPN cihazı markasına, modeli, bellenim sürümünü alır ve müşterilerin Şirket içi VPN aygıtlarına doğrudan uygulayacakları ilgili yapılandırma betiğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="02a5b-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="02a5b-108">Komut dosyası seçili aygıtın söz dizimini alır ve Azure ağ geçidi genel IP adresleri, sanal ağ adresi önekleri, VPN tüneli önceden paylaşılan anahtarı vb. gibi gerekli parametreleri doldurur</span><span class="sxs-lookup"><span data-stu-id="02a5b-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="02a5b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02a5b-109">EXAMPLES</span></span>

### <span data-ttu-id="02a5b-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="02a5b-110">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="02a5b-111">Yukarıdaki örnekte, desteklenen VPN cihaz markalarının, modellerin ve bellenim sürümlerinin alınması için Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice kullanılır.</span><span class="sxs-lookup"><span data-stu-id="02a5b-111">The above example uses Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="02a5b-112">Daha sonra VirtualNetworkGatewayConnection "TestConnection" için bir VPN cihaz yapılandırması oluşturmak için döndürülen model bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="02a5b-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="02a5b-113">Bu örnekte kullanılan cihazda DeviceFamily "IOS-test", Devicevenun "Cisco-test" ve FirmwareVersion 20 bulunur.</span><span class="sxs-lookup"><span data-stu-id="02a5b-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="02a5b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02a5b-114">PARAMETERS</span></span>

### <span data-ttu-id="02a5b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a5b-115">-DefaultProfile</span></span>
<span data-ttu-id="02a5b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02a5b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02a5b-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="02a5b-117">-DeviceFamily</span></span>
<span data-ttu-id="02a5b-118">VPN cihaz modelinin/ailesinin adı.</span><span class="sxs-lookup"><span data-stu-id="02a5b-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="02a5b-119">-Devicevençi</span><span class="sxs-lookup"><span data-stu-id="02a5b-119">-DeviceVendor</span></span>
<span data-ttu-id="02a5b-120">VPN cihazı üreticisinin adı.</span><span class="sxs-lookup"><span data-stu-id="02a5b-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="02a5b-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="02a5b-121">-FirmwareVersion</span></span>
<span data-ttu-id="02a5b-122">VPN aygıtının bellenim sürümü.</span><span class="sxs-lookup"><span data-stu-id="02a5b-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="02a5b-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="02a5b-123">-Name</span></span>
<span data-ttu-id="02a5b-124">Yapılandırma oluşturulacak bağlantının kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="02a5b-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="02a5b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02a5b-125">-ResourceGroupName</span></span>
<span data-ttu-id="02a5b-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="02a5b-126">The resource group name.</span></span>

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

### <span data-ttu-id="02a5b-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="02a5b-127">-Confirm</span></span>
<span data-ttu-id="02a5b-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="02a5b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02a5b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02a5b-129">-WhatIf</span></span>
<span data-ttu-id="02a5b-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="02a5b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02a5b-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="02a5b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02a5b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a5b-132">CommonParameters</span></span>
<span data-ttu-id="02a5b-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02a5b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a5b-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02a5b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a5b-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02a5b-135">INPUTS</span></span>

### <span data-ttu-id="02a5b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="02a5b-136">System.String</span></span>

## <span data-ttu-id="02a5b-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02a5b-137">OUTPUTS</span></span>

### <span data-ttu-id="02a5b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="02a5b-138">System.String</span></span>

## <span data-ttu-id="02a5b-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02a5b-139">NOTES</span></span>

## <span data-ttu-id="02a5b-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02a5b-140">RELATED LINKS</span></span>

