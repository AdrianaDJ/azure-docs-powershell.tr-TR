---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: f4bc62c1675743c62e4e26415435d48ef52034ee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918423"
---
# <span data-ttu-id="95403-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="95403-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="95403-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95403-102">SYNOPSIS</span></span>
<span data-ttu-id="95403-103">Bu komut, bağlantı kaynağını, VPN cihazı markasına, modeli, bellenim sürümünü alır ve müşterilerin Şirket içi VPN aygıtlarına doğrudan uygulayacakları ilgili yapılandırma betiğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="95403-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="95403-104">Komut dosyası seçili aygıtın söz dizimini alır ve Azure ağ geçidi genel IP adresleri, sanal ağ adresi önekleri, VPN tüneli önceden paylaşılan anahtarı vb. gibi gerekli parametreleri doldurur</span><span class="sxs-lookup"><span data-stu-id="95403-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="95403-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95403-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95403-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="95403-106">DESCRIPTION</span></span>
<span data-ttu-id="95403-107">Bu komut, bağlantı kaynağını, VPN cihazı markasına, modeli, bellenim sürümünü alır ve müşterilerin Şirket içi VPN aygıtlarına doğrudan uygulayacakları ilgili yapılandırma betiğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="95403-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="95403-108">Komut dosyası seçili aygıtın söz dizimini alır ve Azure ağ geçidi genel IP adresleri, sanal ağ adresi önekleri, VPN tüneli önceden paylaşılan anahtarı vb. gibi gerekli parametreleri doldurur</span><span class="sxs-lookup"><span data-stu-id="95403-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="95403-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95403-109">EXAMPLES</span></span>

### <span data-ttu-id="95403-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="95403-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="95403-111">Yukarıdaki örnekte, desteklenen VPN cihaz markalarının, modellerin ve bellenim sürümlerinin alınması için Get-AzVirtualNetworkGatewaySupportedVpnDevice kullanılır.</span><span class="sxs-lookup"><span data-stu-id="95403-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="95403-112">Daha sonra VirtualNetworkGatewayConnection "TestConnection" için bir VPN cihaz yapılandırması oluşturmak için döndürülen model bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="95403-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="95403-113">Bu örnekte kullanılan cihazda DeviceFamily "IOS-test", Devicevenun "Cisco-test" ve FirmwareVersion 20 bulunur.</span><span class="sxs-lookup"><span data-stu-id="95403-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="95403-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95403-114">PARAMETERS</span></span>

### <span data-ttu-id="95403-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95403-115">-DefaultProfile</span></span>
<span data-ttu-id="95403-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="95403-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95403-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="95403-117">-DeviceFamily</span></span>
<span data-ttu-id="95403-118">VPN cihaz modelinin/ailesinin adı.</span><span class="sxs-lookup"><span data-stu-id="95403-118">Name of the VPN device model/family.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95403-119">-Devicevençi</span><span class="sxs-lookup"><span data-stu-id="95403-119">-DeviceVendor</span></span>
<span data-ttu-id="95403-120">VPN cihazı üreticisinin adı.</span><span class="sxs-lookup"><span data-stu-id="95403-120">Name of the VPN device vendor.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95403-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="95403-121">-FirmwareVersion</span></span>
<span data-ttu-id="95403-122">VPN aygıtının bellenim sürümü.</span><span class="sxs-lookup"><span data-stu-id="95403-122">Firmware version of the VPN device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95403-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="95403-123">-Name</span></span>
<span data-ttu-id="95403-124">Yapılandırma oluşturulacak bağlantının kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="95403-124">The resource name of the connection for which the configuration is to be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95403-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95403-125">-ResourceGroupName</span></span>
<span data-ttu-id="95403-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="95403-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95403-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="95403-127">-Confirm</span></span>
<span data-ttu-id="95403-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="95403-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95403-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95403-129">-WhatIf</span></span>
<span data-ttu-id="95403-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="95403-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95403-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="95403-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95403-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95403-132">CommonParameters</span></span>
<span data-ttu-id="95403-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95403-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95403-134">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="95403-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95403-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95403-135">INPUTS</span></span>

### <span data-ttu-id="95403-136">System. String</span><span class="sxs-lookup"><span data-stu-id="95403-136">System.String</span></span>

## <span data-ttu-id="95403-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95403-137">OUTPUTS</span></span>

### <span data-ttu-id="95403-138">System. String</span><span class="sxs-lookup"><span data-stu-id="95403-138">System.String</span></span>

## <span data-ttu-id="95403-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95403-139">NOTES</span></span>

## <span data-ttu-id="95403-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95403-140">RELATED LINKS</span></span>
