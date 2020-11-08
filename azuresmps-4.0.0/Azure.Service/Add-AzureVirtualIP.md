---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FBED8515-4216-4AB6-B34E-D14A6063A3A7
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2f145ec51bc6744d877661554e3d8e475d722fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105713"
---
# <span data-ttu-id="51ecb-101">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="51ecb-101">Add-AzureVirtualIP</span></span>

## <span data-ttu-id="51ecb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="51ecb-103">Bulut hizmetine sanal IP ekler.</span><span class="sxs-lookup"><span data-stu-id="51ecb-103">Adds a virtual IP to a cloud service.</span></span>

## <span data-ttu-id="51ecb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51ecb-104">SYNTAX</span></span>

```
Add-AzureVirtualIP [-ServiceName] <String> [-VirtualIPName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="51ecb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="51ecb-105">DESCRIPTION</span></span>
<span data-ttu-id="51ecb-106">**Add-AzureVirtualIP** cmdlet 'i Azure hizmetinize yeni BIR sanal IP (VIP) ekler.</span><span class="sxs-lookup"><span data-stu-id="51ecb-106">The **Add-AzureVirtualIP** cmdlet adds a new virtual IP (VIP) to your Azure service.</span></span>
<span data-ttu-id="51ecb-107">Yeni sanal IP bir ada sahip ancak bir IP adresi ayrılmamış.</span><span class="sxs-lookup"><span data-stu-id="51ecb-107">The new virtual IP has a name but is not allocated an IP address.</span></span>

<span data-ttu-id="51ecb-108">IP adresi yalnızca bir uç noktayı VIP ile ilişkilendirirseniz ayrılır.</span><span class="sxs-lookup"><span data-stu-id="51ecb-108">The IP address is allocated only when you associate an endpoint to the VIP.</span></span>
<span data-ttu-id="51ecb-109">Daha fazla bilgi için Add-AzureEndpoint bakın.</span><span class="sxs-lookup"><span data-stu-id="51ecb-109">See Add-AzureEndpoint for more details.</span></span>

<span data-ttu-id="51ecb-110">Aboneliğiniz ekstra VIP 'ler için ücretlendirilecek ve bu da son noktayla ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="51ecb-110">Your subscription is charged for extra VIPs only once they are associated with an endpoint.</span></span>

## <span data-ttu-id="51ecb-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51ecb-111">EXAMPLES</span></span>

### <span data-ttu-id="51ecb-112">Örnek 1: hizmete sanal IP ekleme</span><span class="sxs-lookup"><span data-stu-id="51ecb-112">Example 1: Add a virtual IP to a service</span></span>
```
PS C:\> Add-AzureVirtualIP -VirtualIPName "Vip01" -ServiceName "ContosoService03"
OperationDescription OperationId                          OperationStatus
-------------------- -----------                          ---------------
Add-AzureVirtualIP   4bd7b638-d2e7-216f-ba38-5221233d70ce Succeeded
```

<span data-ttu-id="51ecb-113">Bu komut, bir hizmete sanal IP adresi ekler.</span><span class="sxs-lookup"><span data-stu-id="51ecb-113">This command adds a virtual IP address to a service.</span></span>

## <span data-ttu-id="51ecb-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51ecb-114">PARAMETERS</span></span>

### <span data-ttu-id="51ecb-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="51ecb-115">-InformationAction</span></span>
<span data-ttu-id="51ecb-116">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="51ecb-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="51ecb-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="51ecb-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="51ecb-118">'A</span><span class="sxs-lookup"><span data-stu-id="51ecb-118">Continue</span></span>
- <span data-ttu-id="51ecb-119">Manıza</span><span class="sxs-lookup"><span data-stu-id="51ecb-119">Ignore</span></span>
- <span data-ttu-id="51ecb-120">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="51ecb-120">Inquire</span></span>
- <span data-ttu-id="51ecb-121">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="51ecb-121">SilentlyContinue</span></span>
- <span data-ttu-id="51ecb-122">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="51ecb-122">Stop</span></span>
- <span data-ttu-id="51ecb-123">Biliriz</span><span class="sxs-lookup"><span data-stu-id="51ecb-123">Suspend</span></span>

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

### <span data-ttu-id="51ecb-124">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="51ecb-124">-InformationVariable</span></span>
<span data-ttu-id="51ecb-125">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="51ecb-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="51ecb-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="51ecb-126">-Profile</span></span>
<span data-ttu-id="51ecb-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="51ecb-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="51ecb-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="51ecb-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="51ecb-129">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="51ecb-129">-ServiceName</span></span>
<span data-ttu-id="51ecb-130">Hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51ecb-130">Specifies the name of the service.</span></span>

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

### <span data-ttu-id="51ecb-131">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="51ecb-131">-VirtualIPName</span></span>
<span data-ttu-id="51ecb-132">Sanal IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51ecb-132">Specifies the name of the virtual IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51ecb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51ecb-133">CommonParameters</span></span>
<span data-ttu-id="51ecb-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51ecb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51ecb-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51ecb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51ecb-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51ecb-136">INPUTS</span></span>

## <span data-ttu-id="51ecb-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51ecb-137">OUTPUTS</span></span>

### <span data-ttu-id="51ecb-138">Microsoft. Windowsazme. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="51ecb-138">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="51ecb-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51ecb-139">NOTES</span></span>

## <span data-ttu-id="51ecb-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51ecb-140">RELATED LINKS</span></span>

[<span data-ttu-id="51ecb-141">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="51ecb-141">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="51ecb-142">Remove-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="51ecb-142">Remove-AzureVirtualIP</span></span>](./Remove-AzureVirtualIP.md)


