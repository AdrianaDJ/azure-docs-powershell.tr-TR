---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 184FB33A-C866-4AF0-BA31-8ADCFC6EE8E2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15ce5d8511383ad93e288b97381416d7864c3f80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105646"
---
# <span data-ttu-id="43338-101">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="43338-101">Get-AzureDns</span></span>

## <span data-ttu-id="43338-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43338-102">SYNOPSIS</span></span>
<span data-ttu-id="43338-103">Azure dağıtımının DNS ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="43338-103">Gets the DNS settings for an Azure deployment.</span></span>

## <span data-ttu-id="43338-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="43338-104">SYNTAX</span></span>

```
Get-AzureDns [-DnsSettings <DnsSettings>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="43338-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="43338-105">DESCRIPTION</span></span>
<span data-ttu-id="43338-106">**Get-AzureDns** cmdlet 'ı bir Azure dağıtımının DNS ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="43338-106">The **Get-AzureDns** cmdlet gets the DNS settings for an Azure deployment.</span></span>
<span data-ttu-id="43338-107">Cmdlet, DNS Ayarları nesnesindeki DNS sunucusunun kolay adını ve IP adresini döndürür.</span><span class="sxs-lookup"><span data-stu-id="43338-107">The cmdlet returns the friendly name and IP address of the DNS server in a DNS settings object.</span></span>

## <span data-ttu-id="43338-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="43338-108">EXAMPLES</span></span>

### <span data-ttu-id="43338-109">Örnek 1: DNS ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="43338-109">Example 1: Get DNS settings</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Production" | Get-AzureDNS
```

<span data-ttu-id="43338-110">Bu komut, ContosoService adlı hizmetin üretim dağıtımını almak için **Get-AzureDeployment** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="43338-110">This command uses the **Get-AzureDeployment** cmdlet to get the production deployment of the service named ContosoService.</span></span>
<span data-ttu-id="43338-111">Komut, ardışık düzen işlecini kullanarak nesneyi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="43338-111">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="43338-112">Geçerli cmdlet, DNS ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="43338-112">The current cmdlet gets the DNS settings.</span></span>

## <span data-ttu-id="43338-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="43338-113">PARAMETERS</span></span>

### <span data-ttu-id="43338-114">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="43338-114">-DnsSettings</span></span>
<span data-ttu-id="43338-115">Bir **Dnssettings** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="43338-115">Specifies a **DnsSettings** object.</span></span>

```yaml
Type: DnsSettings
Parameter Sets: (All)
Aliases: InputObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43338-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="43338-116">-InformationAction</span></span>
<span data-ttu-id="43338-117">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="43338-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="43338-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="43338-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43338-119">'A</span><span class="sxs-lookup"><span data-stu-id="43338-119">Continue</span></span>
- <span data-ttu-id="43338-120">Manıza</span><span class="sxs-lookup"><span data-stu-id="43338-120">Ignore</span></span>
- <span data-ttu-id="43338-121">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="43338-121">Inquire</span></span>
- <span data-ttu-id="43338-122">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="43338-122">SilentlyContinue</span></span>
- <span data-ttu-id="43338-123">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="43338-123">Stop</span></span>
- <span data-ttu-id="43338-124">Biliriz</span><span class="sxs-lookup"><span data-stu-id="43338-124">Suspend</span></span>

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

### <span data-ttu-id="43338-125">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="43338-125">-InformationVariable</span></span>
<span data-ttu-id="43338-126">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="43338-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="43338-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43338-127">CommonParameters</span></span>
<span data-ttu-id="43338-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="43338-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43338-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43338-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43338-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="43338-130">INPUTS</span></span>

## <span data-ttu-id="43338-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="43338-131">OUTPUTS</span></span>

## <span data-ttu-id="43338-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="43338-132">NOTES</span></span>

## <span data-ttu-id="43338-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="43338-133">RELATED LINKS</span></span>

[<span data-ttu-id="43338-134">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="43338-134">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="43338-135">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="43338-135">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="43338-136">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="43338-136">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="43338-137">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="43338-137">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="43338-138">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="43338-138">Set-AzureDns</span></span>](./Set-AzureDns.md)


