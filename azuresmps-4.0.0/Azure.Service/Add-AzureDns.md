---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AF4DF7EC-95BA-44E2-AB9B-5C8FE45CCE4C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83c0858d813c157301098f680fa9d2a90ef6950a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105734"
---
# <span data-ttu-id="4db06-101">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="4db06-101">Add-AzureDns</span></span>

## <span data-ttu-id="4db06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4db06-102">SYNOPSIS</span></span>
<span data-ttu-id="4db06-103">Azure hizmetine DNS sunucusu ekler.</span><span class="sxs-lookup"><span data-stu-id="4db06-103">Adds a DNS server to an Azure service.</span></span>

## <span data-ttu-id="4db06-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4db06-104">SYNTAX</span></span>

```
Add-AzureDns [-Name] <String> [-IPAddress] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4db06-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4db06-105">DESCRIPTION</span></span>
<span data-ttu-id="4db06-106">**Add-AzureDns** cmdlet 'ı bir Azure hizmetine DNS sunucusu ekler.</span><span class="sxs-lookup"><span data-stu-id="4db06-106">The **Add-AzureDns** cmdlet adds a DNS server to an Azure service.</span></span>

## <span data-ttu-id="4db06-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4db06-107">EXAMPLES</span></span>

### <span data-ttu-id="4db06-108">Örnek 1: DNS sunucusu ekleme</span><span class="sxs-lookup"><span data-stu-id="4db06-108">Example 1: Add a DNS server</span></span>
```
PS C:\> Add-AzureDns -ServiceName "ContosoService" -IPAddress 10.1.2.4 -Name "Dns07"
```

<span data-ttu-id="4db06-109">Bu komut, 10.1.2.4 adresine sahip olan DNS sunucusunu ContosoService 'e ekler.</span><span class="sxs-lookup"><span data-stu-id="4db06-109">This command adds the DNS server that has the address 10.1.2.4 to ContosoService.</span></span>

## <span data-ttu-id="4db06-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4db06-110">PARAMETERS</span></span>

### <span data-ttu-id="4db06-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="4db06-111">-InformationAction</span></span>
<span data-ttu-id="4db06-112">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4db06-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4db06-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4db06-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4db06-114">'A</span><span class="sxs-lookup"><span data-stu-id="4db06-114">Continue</span></span>
- <span data-ttu-id="4db06-115">Manıza</span><span class="sxs-lookup"><span data-stu-id="4db06-115">Ignore</span></span>
- <span data-ttu-id="4db06-116">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="4db06-116">Inquire</span></span>
- <span data-ttu-id="4db06-117">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="4db06-117">SilentlyContinue</span></span>
- <span data-ttu-id="4db06-118">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="4db06-118">Stop</span></span>
- <span data-ttu-id="4db06-119">Biliriz</span><span class="sxs-lookup"><span data-stu-id="4db06-119">Suspend</span></span>

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

### <span data-ttu-id="4db06-120">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="4db06-120">-InformationVariable</span></span>
<span data-ttu-id="4db06-121">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="4db06-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4db06-122">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="4db06-122">-IPAddress</span></span>
<span data-ttu-id="4db06-123">DNS sunucusunun IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4db06-123">Specifies the IP address of the DNS server.</span></span>

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

### <span data-ttu-id="4db06-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="4db06-124">-Name</span></span>
<span data-ttu-id="4db06-125">DNS sunucusu için kolay bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="4db06-125">Specifies a friendly name for the DNS server.</span></span>
<span data-ttu-id="4db06-126">Bu ad tam nitelikli bir etki alanı adı değildir.</span><span class="sxs-lookup"><span data-stu-id="4db06-126">This name is not necessarily a fully qualified domain name.</span></span>

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

### <span data-ttu-id="4db06-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="4db06-127">-Profile</span></span>
<span data-ttu-id="4db06-128">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4db06-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4db06-129">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="4db06-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4db06-130">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="4db06-130">-ServiceName</span></span>
<span data-ttu-id="4db06-131">Bu cmdlet 'in DNS sunucusunu eklediği hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4db06-131">Specifies the name of the service to which this cmdlet adds the DNS server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4db06-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4db06-132">CommonParameters</span></span>
<span data-ttu-id="4db06-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4db06-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4db06-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4db06-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4db06-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4db06-135">INPUTS</span></span>

## <span data-ttu-id="4db06-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4db06-136">OUTPUTS</span></span>

### <span data-ttu-id="4db06-137">Microsoft. Windowsazme. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="4db06-137">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="4db06-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4db06-138">NOTES</span></span>

## <span data-ttu-id="4db06-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4db06-139">RELATED LINKS</span></span>

[<span data-ttu-id="4db06-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="4db06-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="4db06-141">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="4db06-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="4db06-142">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="4db06-142">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="4db06-143">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="4db06-143">Set-AzureDns</span></span>](./Set-AzureDns.md)


