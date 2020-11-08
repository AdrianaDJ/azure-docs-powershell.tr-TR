---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4522E93F-6AC9-4A37-88B8-CCCCE15A5879
online version: ''
schema: 2.0.0
ms.openlocfilehash: fcfc41e06f6847612c275817560e8593b76f6bac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105471"
---
# <span data-ttu-id="000c7-101">Reset-AzureRemoteAppVpnSharedKey</span><span class="sxs-lookup"><span data-stu-id="000c7-101">Reset-AzureRemoteAppVpnSharedKey</span></span>

## <span data-ttu-id="000c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="000c7-102">SYNOPSIS</span></span>
<span data-ttu-id="000c7-103">Azure RemoteApp VPN paylaşılan anahtarını sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="000c7-103">Resets the Azure RemoteApp VPN shared key.</span></span>

## <span data-ttu-id="000c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="000c7-104">SYNTAX</span></span>

```
Reset-AzureRemoteAppVpnSharedKey [-VNetName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="000c7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="000c7-105">DESCRIPTION</span></span>
<span data-ttu-id="000c7-106">**Reset-AzureRemoteAppVpnSharedKey** cmdlet 'ı, Azure RemoteApp sanal özel ağ (VPN) paylaşılan anahtarını sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="000c7-106">The **Reset-AzureRemoteAppVpnSharedKey** cmdlet resets the Azure RemoteApp virtual private network (VPN) shared key.</span></span>

## <span data-ttu-id="000c7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="000c7-107">EXAMPLES</span></span>

### <span data-ttu-id="000c7-108">Örnek 1: sanal ağdaki paylaşılan anahtarı sıfırlama</span><span class="sxs-lookup"><span data-stu-id="000c7-108">Example 1: Reset the shared key on a virtual network</span></span>
```
PS C:\> Reset-AzureRemoteAppVpnSharedKey -VNetName "ContosoVNet"
```

<span data-ttu-id="000c7-109">Bu komut, ContosoVNet adlı sanal ağdaki paylaşılan anahtarı sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="000c7-109">This command resets the shared key on the virtual network named ContosoVNet.</span></span>
<span data-ttu-id="000c7-110">VPN cihazında yeni paylaşılan anahtar yapılandırılmadığı sürece Şirket içi ağa VPN bağlantısı çevrimdışı kalır.</span><span class="sxs-lookup"><span data-stu-id="000c7-110">The VPN connection to the on-premises network remains offline until the new shared key is configured on the VPN device.</span></span>
<span data-ttu-id="000c7-111">VPN aygıtını yapılandırmak için, VPN aygıtınızın doğru kodunu veya yapılandırma dosyasını almak üzere **Get-Azureremoteappvpndeviceconfigscrıpt** cmdlet 'ini kullanın, ardından bu komut dosyasını veya yapılandırma dosyasını VPN aygıtına yükleyin.</span><span class="sxs-lookup"><span data-stu-id="000c7-111">To configure the VPN device, use the **Get-AzureRemoteAppVpnDeviceConfigScript** cmdlet to retrieve the correct script or configuration file for your VPN device, then load that script or configuration file onto the VPN device.</span></span>

## <span data-ttu-id="000c7-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="000c7-112">PARAMETERS</span></span>

### <span data-ttu-id="000c7-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="000c7-113">-Profile</span></span>
<span data-ttu-id="000c7-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="000c7-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="000c7-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="000c7-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="000c7-116">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="000c7-116">-VNetName</span></span>
<span data-ttu-id="000c7-117">Azure RemoteApp sanal ağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="000c7-117">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="000c7-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="000c7-118">-Confirm</span></span>
<span data-ttu-id="000c7-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="000c7-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="000c7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="000c7-120">-WhatIf</span></span>
<span data-ttu-id="000c7-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="000c7-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="000c7-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="000c7-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="000c7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="000c7-123">CommonParameters</span></span>
<span data-ttu-id="000c7-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="000c7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="000c7-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="000c7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="000c7-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="000c7-126">INPUTS</span></span>

## <span data-ttu-id="000c7-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="000c7-127">OUTPUTS</span></span>

### <span data-ttu-id="000c7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="000c7-128">System.String</span></span>

## <span data-ttu-id="000c7-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="000c7-129">NOTES</span></span>

## <span data-ttu-id="000c7-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="000c7-130">RELATED LINKS</span></span>

[<span data-ttu-id="000c7-131">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="000c7-131">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="000c7-132">Get-Azureremoteappvpndeviceconfigscrıpt</span><span class="sxs-lookup"><span data-stu-id="000c7-132">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>](./Get-AzureRemoteAppVpnDeviceConfigScript.md)


