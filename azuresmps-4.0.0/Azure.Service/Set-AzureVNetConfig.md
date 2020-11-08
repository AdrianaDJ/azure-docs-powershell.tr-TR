---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 895F9A5F-D48F-403D-BD8F-72D72D420690
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97bb3e07f5c6df25e7c03c167cc4cb49c25f9414
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105787"
---
# <span data-ttu-id="844bd-101">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="844bd-101">Set-AzureVNetConfig</span></span>

## <span data-ttu-id="844bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="844bd-102">SYNOPSIS</span></span>
<span data-ttu-id="844bd-103">Bir Azure bulut hizmeti için sanal ağ ayarlarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="844bd-103">Updates the virtual network settings for an Azure cloud service.</span></span>

## <span data-ttu-id="844bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="844bd-104">SYNTAX</span></span>

```
Set-AzureVNetConfig [-ConfigurationPath] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="844bd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="844bd-105">DESCRIPTION</span></span>
<span data-ttu-id="844bd-106">**Set-AzureVNetConfig** cmdlet 'i, ağ yapılandırma dosyasının (. netcfg) yolunu belirterek geçerli Azure aboneliğinin ağ yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="844bd-106">The **Set-AzureVNetConfig** cmdlet updates the network configuration for the current Azure subscription by specifying a path to a network configuration file (.netcfg).</span></span>
<span data-ttu-id="844bd-107">Ağ yapılandırma dosyası, abonelik içinde bulut hizmetleri için DNS sunucularını ve alt ağlarını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="844bd-107">The network configuration file defines DNS servers and subnets for cloud services within a subscription.</span></span>

## <span data-ttu-id="844bd-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="844bd-108">EXAMPLES</span></span>

### <span data-ttu-id="844bd-109">Örnek 1: Azure aboneliğinin ağ yapılandırmasını yerel bir dosyaya güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="844bd-109">Example 1: Update the network configuration of the Azure subscription to a local file</span></span>
```
PS C:\> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="844bd-110">Bu komut, geçerli Microsoft Azure aboneliğinin ağ yapılandırmasını "c:\temp\MyAzNets.netcfg" yerel dosyasıyla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="844bd-110">This command updates the network configuration of the current Microsoft Azure subscription to that in the local file "c:\temp\MyAzNets.netcfg".</span></span>

### <span data-ttu-id="844bd-111">Örnek 2: Azure aboneliğini ayarlayın ve ardından ağ yapılandırmasını güncelleyin</span><span class="sxs-lookup"><span data-stu-id="844bd-111">Example 2: Set the Azure subscription and then update the network configuration</span></span>
```
PS C:\> $SubsId = "5bea2bc2-88a5-44b8-abe1-3e76733b6783"
C:\PS> $Cert = Get-Item cert:\LocalMachine\MY\82F105B2DA81149204A6257A9A91EC452B8C52C3
C:\PS> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="844bd-112">Bu örnekte, Microsoft Azure aboneliği ayarlanır ve ardından "c:\temp\MyAzNets.netcfg" yerel dosyasında tanımlanan yapılandırmayı kullanarak bu aboneliğin ağ yapılandırması güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="844bd-112">This example sets the Microsoft Azure subscription, and then updates the network configuration of that subscription using the configuration defined in the local file "c:\temp\MyAzNets.netcfg".</span></span>

## <span data-ttu-id="844bd-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="844bd-113">PARAMETERS</span></span>

### <span data-ttu-id="844bd-114">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="844bd-114">-ConfigurationPath</span></span>
<span data-ttu-id="844bd-115">Ağ yapılandırma dosyasının (. netcfg) yolunu ve dosya adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="844bd-115">Specifies the path and file name of a network configuration file (.netcfg).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="844bd-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="844bd-116">-InformationAction</span></span>
<span data-ttu-id="844bd-117">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="844bd-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="844bd-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="844bd-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="844bd-119">'A</span><span class="sxs-lookup"><span data-stu-id="844bd-119">Continue</span></span>
- <span data-ttu-id="844bd-120">Manıza</span><span class="sxs-lookup"><span data-stu-id="844bd-120">Ignore</span></span>
- <span data-ttu-id="844bd-121">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="844bd-121">Inquire</span></span>
- <span data-ttu-id="844bd-122">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="844bd-122">SilentlyContinue</span></span>
- <span data-ttu-id="844bd-123">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="844bd-123">Stop</span></span>
- <span data-ttu-id="844bd-124">Biliriz</span><span class="sxs-lookup"><span data-stu-id="844bd-124">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="844bd-125">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="844bd-125">-InformationVariable</span></span>
<span data-ttu-id="844bd-126">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="844bd-126">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="844bd-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="844bd-127">-Profile</span></span>
<span data-ttu-id="844bd-128">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="844bd-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="844bd-129">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="844bd-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="844bd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="844bd-130">CommonParameters</span></span>
<span data-ttu-id="844bd-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="844bd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="844bd-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="844bd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="844bd-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="844bd-133">INPUTS</span></span>

## <span data-ttu-id="844bd-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="844bd-134">OUTPUTS</span></span>

## <span data-ttu-id="844bd-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="844bd-135">NOTES</span></span>

## <span data-ttu-id="844bd-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="844bd-136">RELATED LINKS</span></span>

[<span data-ttu-id="844bd-137">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="844bd-137">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="844bd-138">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="844bd-138">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="844bd-139">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="844bd-139">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)


