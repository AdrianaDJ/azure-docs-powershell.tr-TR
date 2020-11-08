---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1085388B-0855-4E29-9043-3FE2C638F58D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22c97045cb5f85256ec4d252cdbfb13c59643008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105924"
---
# <span data-ttu-id="686e7-101">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="686e7-101">New-AzureDns</span></span>

## <span data-ttu-id="686e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="686e7-102">SYNOPSIS</span></span>
<span data-ttu-id="686e7-103">Azure DNS ayarları nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="686e7-103">Creates an Azure DNS settings object.</span></span>

## <span data-ttu-id="686e7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="686e7-104">SYNTAX</span></span>

```
New-AzureDns [-Name] <String> [-IPAddress] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="686e7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="686e7-105">DESCRIPTION</span></span>
<span data-ttu-id="686e7-106">**New-AzureDns** cmdlet 'ı BIR Azure DNS ayarları nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="686e7-106">The **New-AzureDns** cmdlet creates an Azure DNS settings object.</span></span>
<span data-ttu-id="686e7-107">**New-AzureVM** cmdlet 'ini kullanarak bir sanal makıne oluştururken DNS ayarları nesnesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="686e7-107">You can use a DNS settings object when you create a virtual machine by using the **New-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="686e7-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="686e7-108">EXAMPLES</span></span>

### <span data-ttu-id="686e7-109">Örnek 1: DNS ayarları nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="686e7-109">Example 1: Create a DNS settings object</span></span>
```
PS C:\> $Dns = New-AzureDns -Name "Dns01" -IPAddress "10.1.2.4"
```

<span data-ttu-id="686e7-110">Bu komut, bir Azure DNS ayarları nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="686e7-110">This command creates an Azure DNS settings object.</span></span>
<span data-ttu-id="686e7-111">DNS sunucusu belirtilen adres ve kolay ad Dns01.</span><span class="sxs-lookup"><span data-stu-id="686e7-111">The DNS server has the specified address and the friendly name Dns01.</span></span>
<span data-ttu-id="686e7-112">Komut, $Dns değişkeninde, **New-AzureVM** cmdlet 'i tarafından kullanılmak üzere depolar.</span><span class="sxs-lookup"><span data-stu-id="686e7-112">The command stores the object in the $Dns variable for use by the **New-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="686e7-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="686e7-113">PARAMETERS</span></span>

### <span data-ttu-id="686e7-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="686e7-114">-InformationAction</span></span>
<span data-ttu-id="686e7-115">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="686e7-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="686e7-116">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="686e7-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="686e7-117">'A</span><span class="sxs-lookup"><span data-stu-id="686e7-117">Continue</span></span>
- <span data-ttu-id="686e7-118">Manıza</span><span class="sxs-lookup"><span data-stu-id="686e7-118">Ignore</span></span>
- <span data-ttu-id="686e7-119">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="686e7-119">Inquire</span></span>
- <span data-ttu-id="686e7-120">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="686e7-120">SilentlyContinue</span></span>
- <span data-ttu-id="686e7-121">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="686e7-121">Stop</span></span>
- <span data-ttu-id="686e7-122">Biliriz</span><span class="sxs-lookup"><span data-stu-id="686e7-122">Suspend</span></span>

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

### <span data-ttu-id="686e7-123">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="686e7-123">-InformationVariable</span></span>
<span data-ttu-id="686e7-124">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="686e7-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="686e7-125">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="686e7-125">-IPAddress</span></span>
<span data-ttu-id="686e7-126">DNS sunucusunun IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="686e7-126">Specifies the IP address of the DNS server.</span></span>

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

### <span data-ttu-id="686e7-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="686e7-127">-Name</span></span>
<span data-ttu-id="686e7-128">DNS sunucusu için kolay bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="686e7-128">Specifies a friendly name for the DNS server.</span></span>
<span data-ttu-id="686e7-129">Bu ad tam nitelikli bir etki alanı adı değildir.</span><span class="sxs-lookup"><span data-stu-id="686e7-129">This name is not necessarily a fully qualified domain name.</span></span>

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

### <span data-ttu-id="686e7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="686e7-130">CommonParameters</span></span>
<span data-ttu-id="686e7-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="686e7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="686e7-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="686e7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="686e7-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="686e7-133">INPUTS</span></span>

## <span data-ttu-id="686e7-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="686e7-134">OUTPUTS</span></span>

## <span data-ttu-id="686e7-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="686e7-135">NOTES</span></span>

## <span data-ttu-id="686e7-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="686e7-136">RELATED LINKS</span></span>

[<span data-ttu-id="686e7-137">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="686e7-137">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="686e7-138">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="686e7-138">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="686e7-139">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="686e7-139">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="686e7-140">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="686e7-140">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="686e7-141">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="686e7-141">Set-AzureDns</span></span>](./Set-AzureDns.md)


