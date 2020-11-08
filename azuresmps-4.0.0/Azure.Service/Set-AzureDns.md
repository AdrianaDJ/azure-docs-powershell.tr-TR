---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5BC16303-CCB4-40D8-ABCB-59CF0D85ED63
online version: ''
schema: 2.0.0
ms.openlocfilehash: f24f5d8f7f72c59847cfa5dde51a1937bc304735
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106069"
---
# <span data-ttu-id="e32c3-101">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e32c3-101">Set-AzureDns</span></span>

## <span data-ttu-id="e32c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e32c3-102">SYNOPSIS</span></span>
<span data-ttu-id="e32c3-103">DNS sunucusunun IP adresini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e32c3-103">Modifies the IP address of a DNS server.</span></span>

## <span data-ttu-id="e32c3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e32c3-104">SYNTAX</span></span>

```
Set-AzureDns [-Name] <String> [-IPAddress] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e32c3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e32c3-105">DESCRIPTION</span></span>
<span data-ttu-id="e32c3-106">**Set-AzureDns** cmdlet 'i, bir Azure HIZMETI için DNS sunucusunun IP adresini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e32c3-106">The **Set-AzureDns** cmdlet modifies the IP address of a DNS server for an Azure service.</span></span>

## <span data-ttu-id="e32c3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e32c3-107">EXAMPLES</span></span>

### <span data-ttu-id="e32c3-108">Örnek 1: DNS sunucusunun IP adresini değiştirme</span><span class="sxs-lookup"><span data-stu-id="e32c3-108">Example 1: Modify the IP address of a DNS server</span></span>
```
PS C:\> Set-AzureDns -ServiceName "ContosoService" -IPAddress 10.1.2.5 -Name "Dns07"
```

<span data-ttu-id="e32c3-109">Bu komut, ContosoService adındaki hizmet için Dns07 adındaki DNS sunucusunun IP adresini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e32c3-109">This command modifies the IP address of the DNS server named Dns07 for the service named ContosoService.</span></span>

## <span data-ttu-id="e32c3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e32c3-110">PARAMETERS</span></span>

### <span data-ttu-id="e32c3-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="e32c3-111">-InformationAction</span></span>
<span data-ttu-id="e32c3-112">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e32c3-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e32c3-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e32c3-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e32c3-114">'A</span><span class="sxs-lookup"><span data-stu-id="e32c3-114">Continue</span></span>
- <span data-ttu-id="e32c3-115">Manıza</span><span class="sxs-lookup"><span data-stu-id="e32c3-115">Ignore</span></span>
- <span data-ttu-id="e32c3-116">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="e32c3-116">Inquire</span></span>
- <span data-ttu-id="e32c3-117">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="e32c3-117">SilentlyContinue</span></span>
- <span data-ttu-id="e32c3-118">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="e32c3-118">Stop</span></span>
- <span data-ttu-id="e32c3-119">Biliriz</span><span class="sxs-lookup"><span data-stu-id="e32c3-119">Suspend</span></span>

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

### <span data-ttu-id="e32c3-120">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="e32c3-120">-InformationVariable</span></span>
<span data-ttu-id="e32c3-121">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="e32c3-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e32c3-122">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="e32c3-122">-IPAddress</span></span>
<span data-ttu-id="e32c3-123">DNS sunucusunun yeni IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e32c3-123">Specifies the new IP address of the DNS server.</span></span>

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

### <span data-ttu-id="e32c3-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="e32c3-124">-Name</span></span>
<span data-ttu-id="e32c3-125">Bu cmdlet 'in değiştirdiği DNS sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e32c3-125">Specifies the name of the DNS server that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e32c3-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="e32c3-126">-Profile</span></span>
<span data-ttu-id="e32c3-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e32c3-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e32c3-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e32c3-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e32c3-129">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="e32c3-129">-ServiceName</span></span>
<span data-ttu-id="e32c3-130">Bu cmdlet 'in DNS sunucusunun adresini değiştirdiği hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e32c3-130">Specifies the name of the service for which this cmdlet modifies the address of the DNS server.</span></span>

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

### <span data-ttu-id="e32c3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e32c3-131">CommonParameters</span></span>
<span data-ttu-id="e32c3-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e32c3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e32c3-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e32c3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e32c3-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e32c3-134">INPUTS</span></span>

## <span data-ttu-id="e32c3-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e32c3-135">OUTPUTS</span></span>

### <span data-ttu-id="e32c3-136">Microsoft. Windowsazme. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="e32c3-136">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="e32c3-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e32c3-137">NOTES</span></span>

## <span data-ttu-id="e32c3-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e32c3-138">RELATED LINKS</span></span>

[<span data-ttu-id="e32c3-139">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e32c3-139">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="e32c3-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e32c3-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="e32c3-141">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e32c3-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="e32c3-142">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e32c3-142">Remove-AzureDns</span></span>](./Remove-AzureDns.md)


