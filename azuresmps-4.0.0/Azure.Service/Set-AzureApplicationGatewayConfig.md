---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D7D99AFA-A85E-43DA-9F2F-8FFD34048E00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ede675ab58905f102fb9d0029669115acdb9e85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106429"
---
# <span data-ttu-id="d2384-101">Set-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="d2384-101">Set-AzureApplicationGatewayConfig</span></span>

## <span data-ttu-id="d2384-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2384-102">SYNOPSIS</span></span>
<span data-ttu-id="d2384-103">Uygulama ağ geçidi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="d2384-103">Configures an application gateway.</span></span>

## <span data-ttu-id="d2384-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2384-104">SYNTAX</span></span>

### <span data-ttu-id="d2384-105">configFile</span><span class="sxs-lookup"><span data-stu-id="d2384-105">configFile</span></span>
```
Set-AzureApplicationGatewayConfig -Name <String> -ConfigFile <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2384-106">configObject</span><span class="sxs-lookup"><span data-stu-id="d2384-106">configObject</span></span>
```
Set-AzureApplicationGatewayConfig -Name <String> -Config <ApplicationGatewayConfiguration>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d2384-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2384-107">DESCRIPTION</span></span>
<span data-ttu-id="d2384-108">**Set-AzureApplicationGatewayConfig** cmdlet 'i bir uygulama ağ geçidi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="d2384-108">The **Set-AzureApplicationGatewayConfig** cmdlet configures an application gateway.</span></span>

## <span data-ttu-id="d2384-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2384-109">EXAMPLES</span></span>

### <span data-ttu-id="d2384-110">Örnek 1: yapılandırma nesnesi kullanarak uygulama ağ geçidi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d2384-110">Example 1: Configure an application gateway by using a configuration object</span></span>
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway02"
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -Config $ConfigReturnObject
```

<span data-ttu-id="d2384-111">İlk komut **Get-AzureApplicationGatewayConfig** cmdlet 'Ini kullanarak ApplicationGateway02 adındaki uygulama ağ geçidi için yapılandırma nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="d2384-111">The first command gets the configuration object for the application gateway named ApplicationGateway02 by using the **Get-AzureApplicationGatewayConfig** cmdlet.</span></span>
<span data-ttu-id="d2384-112">Komut, $ConfigReturnObject değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d2384-112">The command stores it in the $ConfigReturnObject variable.</span></span>

<span data-ttu-id="d2384-113">İkinci komut, $ConfigReturnObject değişkeninde depolanan bir uygulama ağ geçidi yapılandırma nesnesini kullanarak, ApplicationGateway06 adındaki uygulamanın yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d2384-113">The second command sets the configuration for the application named ApplicationGateway06 by using an application gateway configuration object stored in the $ConfigReturnObject variable.</span></span>

### <span data-ttu-id="d2384-114">Örnek 2: yapılandırma dosyası kullanarak uygulama ağ geçidi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d2384-114">Example 2: Configure an application gateway by using a configuration file</span></span>
```
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ConfigFile "D:\config.xml"
```

<span data-ttu-id="d2384-115">Bu komut, ApplicationGateway06 adındaki uygulamanın yapılandırmasını belirtilen konumda bir uygulama ağ geçidi yapılandırma dosyasını kullanarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d2384-115">This command sets the configuration for the application named ApplicationGateway06 by using an application gateway configuration file in the specified location.</span></span>

### <span data-ttu-id="d2384-116">Örnek 3: yapılandırma nesnesi kullanarak yapılandırmayı değiştirme</span><span class="sxs-lookup"><span data-stu-id="d2384-116">Example 3: Modify a configuration by using a configuration object</span></span>
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
PS C:\> $ConfigReturnObject.Config.FrontendPorts[0].Port = 443
PS C:\> $ConfigReturnObject | Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
```

<span data-ttu-id="d2384-117">İlk komut **Get-AzureApplicationGatewayConfig** cmdlet 'Ini kullanarak ApplicationGateway06 adındaki uygulama ağ geçidi için yapılandırma nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="d2384-117">The first command gets the configuration object for the application gateway named ApplicationGateway06 by using the **Get-AzureApplicationGatewayConfig** cmdlet.</span></span>
<span data-ttu-id="d2384-118">Komut, $ConfigReturnObject değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d2384-118">The command stores it in the $ConfigReturnObject variable.</span></span>

<span data-ttu-id="d2384-119">İkinci komut, $ConfigReturnObject depolanan nesnedeki bir **bağlantı noktası** özelliğine bir bağlantı noktası değeri atar.</span><span class="sxs-lookup"><span data-stu-id="d2384-119">The second command assigns a port value to a **Port** property in the object stored in $ConfigReturnObject.</span></span>

<span data-ttu-id="d2384-120">Son komutu, güncelleştirilmiş $ConfigReturnObject geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="d2384-120">The final command passes the updated $ConfigReturnObject to the current cmdlet.</span></span>

## <span data-ttu-id="d2384-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2384-121">PARAMETERS</span></span>

### <span data-ttu-id="d2384-122">-Config</span><span class="sxs-lookup"><span data-stu-id="d2384-122">-Config</span></span>
<span data-ttu-id="d2384-123">Uygulama ağ geçidi yapılandırma nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2384-123">Specifies an application gateway configuration object.</span></span>
<span data-ttu-id="d2384-124">Bu cmdlet, bu parametrenin bir uygulama ağ geçidine belirttiği yapılandırmayı atar.</span><span class="sxs-lookup"><span data-stu-id="d2384-124">This cmdlet assigns the configuration that this parameter specifies to an application gateway.</span></span>

```yaml
Type: ApplicationGatewayConfiguration
Parameter Sets: configObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2384-125">-Configfıle</span><span class="sxs-lookup"><span data-stu-id="d2384-125">-ConfigFile</span></span>
<span data-ttu-id="d2384-126">Uygulama ağ geçidi için yapılandırma dosyasının yolunu XML biçiminde belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2384-126">Specifies the path of a configuration file, in XML format, for an application gateway.</span></span>
<span data-ttu-id="d2384-127">Bu cmdlet, bu parametrenin bir uygulama ağ geçidine belirttiği yapılandırmayı atar.</span><span class="sxs-lookup"><span data-stu-id="d2384-127">This cmdlet assigns the configuration that this parameter specifies to an application gateway.</span></span>

```yaml
Type: String
Parameter Sets: configFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2384-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="d2384-128">-Name</span></span>
<span data-ttu-id="d2384-129">Bu cmdlet 'in yapılandırdığı uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2384-129">Specifies the name of the application gateway that this cmdlet configures.</span></span>

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

### <span data-ttu-id="d2384-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="d2384-130">-Profile</span></span>
<span data-ttu-id="d2384-131">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2384-131">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d2384-132">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="d2384-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d2384-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2384-133">CommonParameters</span></span>
<span data-ttu-id="d2384-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2384-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2384-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2384-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2384-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2384-136">INPUTS</span></span>

### <span data-ttu-id="d2384-137">System. String, Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2384-137">System.String, Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayConfiguration</span></span>

## <span data-ttu-id="d2384-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2384-138">OUTPUTS</span></span>

### <span data-ttu-id="d2384-139">Microsoft. Windowsazme. Management. ApplicationGateway. model. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d2384-139">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="d2384-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2384-140">NOTES</span></span>

## <span data-ttu-id="d2384-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2384-141">RELATED LINKS</span></span>

[<span data-ttu-id="d2384-142">Get-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="d2384-142">Get-AzureApplicationGatewayConfig</span></span>](./Get-AzureApplicationGatewayConfig.md)


