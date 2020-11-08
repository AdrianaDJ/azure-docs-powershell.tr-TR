---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D0E8B2BD-D68F-477A-9D66-C27AB737960D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59423aa3de5ae91abe82090054fac61f3901363c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105625"
---
# <span data-ttu-id="2b49e-101">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="2b49e-101">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>

## <span data-ttu-id="2b49e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b49e-102">SYNOPSIS</span></span>
<span data-ttu-id="2b49e-103">Azure RemoteApp VPN cihazı için yapılandırma betiğini alır.</span><span class="sxs-lookup"><span data-stu-id="2b49e-103">Retrieves the configuration script for an Azure RemoteApp VPN device.</span></span>

## <span data-ttu-id="2b49e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b49e-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVpnDeviceConfigScript [-VNetName] <String> [-Vendor] <String> [-Platform] <String>
 [-OSFamily] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2b49e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b49e-105">DESCRIPTION</span></span>
<span data-ttu-id="2b49e-106">**Get-AzureRemoteAppVpnDeviceConfigScript** cmdlet 'i, bir Azure RemoteApp sanal özel ağ (VPN) aygıtının yapılandırma betiğini alır.</span><span class="sxs-lookup"><span data-stu-id="2b49e-106">The **Get-AzureRemoteAppVpnDeviceConfigScript** cmdlet retrieves the configuration script for an Azure RemoteApp virtual private network (VPN) device.</span></span>

## <span data-ttu-id="2b49e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b49e-107">EXAMPLES</span></span>

### <span data-ttu-id="2b49e-108">Örnek 1: VPN cihazı için yapılandırma betiği alma</span><span class="sxs-lookup"><span data-stu-id="2b49e-108">Example 1: Get a configuration script for a VPN device</span></span>
```
PS C:\> Get-AzureRemoteAppVpnDeviceConfigScript -VNetName "ContosoVNet" -Vendor "Microsoft Corporation" -OSFamily "Windows Server 2012 R2"
```

<span data-ttu-id="2b49e-109">Bu komut, ContosoVNet adlı sanal ağın VPN aygıtını yapılandırmak için kullanılan kodu veya yapılandırma dosyasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="2b49e-109">This command returns the script or configuration file used to configure the VPN device for the virtual network named ContosoVNet.</span></span>
<span data-ttu-id="2b49e-110">Bu komut dosyası veya yapılandırma dosyası, bu cihaz için genellikle VPN aygıtına çalıştırılmalıdır veya yüklenir.</span><span class="sxs-lookup"><span data-stu-id="2b49e-110">This script or configuration file should be run or loaded onto the VPN device in the typical manner for that device.</span></span>
<span data-ttu-id="2b49e-111">Her aygıtın benzersiz gereksinimleri için VPN cihazı satıcınıza başvurun.</span><span class="sxs-lookup"><span data-stu-id="2b49e-111">Consult the VPN device vendor for the unique requirements for each device.</span></span>

## <span data-ttu-id="2b49e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b49e-112">PARAMETERS</span></span>

### <span data-ttu-id="2b49e-113">-OSFamily</span><span class="sxs-lookup"><span data-stu-id="2b49e-113">-OSFamily</span></span>
<span data-ttu-id="2b49e-114">Cihaz platformunda çalışan işletim sistemi (OS) ailesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b49e-114">Specifies the operating system (OS) family that runs on the device platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b49e-115">-Platform</span><span class="sxs-lookup"><span data-stu-id="2b49e-115">-Platform</span></span>
<span data-ttu-id="2b49e-116">Cihaz platformunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b49e-116">Specifies the device platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b49e-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="2b49e-117">-Profile</span></span>
<span data-ttu-id="2b49e-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b49e-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2b49e-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="2b49e-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2b49e-120">-Satıcı</span><span class="sxs-lookup"><span data-stu-id="2b49e-120">-Vendor</span></span>
<span data-ttu-id="2b49e-121">VPN aygıtının satıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b49e-121">Specifies the vendor of the VPN device.</span></span>

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

### <span data-ttu-id="2b49e-122">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="2b49e-122">-VNetName</span></span>
<span data-ttu-id="2b49e-123">Azure RemoteApp sanal ağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b49e-123">Specifies the name of an Azure RemoteApp virtual network.</span></span>

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

### <span data-ttu-id="2b49e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b49e-124">CommonParameters</span></span>
<span data-ttu-id="2b49e-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2b49e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b49e-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b49e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b49e-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b49e-127">INPUTS</span></span>

## <span data-ttu-id="2b49e-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b49e-128">OUTPUTS</span></span>

## <span data-ttu-id="2b49e-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b49e-129">NOTES</span></span>

## <span data-ttu-id="2b49e-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b49e-130">RELATED LINKS</span></span>

[<span data-ttu-id="2b49e-131">Get-AzureRemoteAppVpnDevice</span><span class="sxs-lookup"><span data-stu-id="2b49e-131">Get-AzureRemoteAppVpnDevice</span></span>](./Get-AzureRemoteAppVpnDevice.md)


