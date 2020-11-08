---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1CFB90FD-7BC5-4687-8D08-775097DDA062
online version: ''
schema: 2.0.0
ms.openlocfilehash: 651b38a21dff03ce3c5925040d65bc2967eeaa77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105645"
---
# <span data-ttu-id="9f2e6-101">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f2e6-101">Get-AzureEndpoint</span></span>

## <span data-ttu-id="9f2e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f2e6-102">SYNOPSIS</span></span>
<span data-ttu-id="9f2e6-103">Bir Azure sanal makinesine atanmış uç noktalar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="9f2e6-103">Gets information about the endpoints that are assigned to an Azure virtual machine.</span></span>

## <span data-ttu-id="9f2e6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f2e6-104">SYNTAX</span></span>

```
Get-AzureEndpoint [[-Name] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9f2e6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f2e6-105">DESCRIPTION</span></span>
<span data-ttu-id="9f2e6-106">**Get-AzureEndpoint** cmdlet 'ı bir Azure sanal makinesine atanmış uç noktalar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="9f2e6-106">The **Get-AzureEndpoint** cmdlet gets information about the endpoints that are assigned to an Azure virtual machine.</span></span>

## <span data-ttu-id="9f2e6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f2e6-107">EXAMPLES</span></span>

### <span data-ttu-id="9f2e6-108">Örnek 1: sanal makine için uç nokta bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="9f2e6-108">Example 1: Get endpoint information for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine12" | Get-AzureEndpoint
```

<span data-ttu-id="9f2e6-109">Bu komut, **Get-AzureVM** cmdlet 'Ini kullanarak VirtualMachine12 adındaki sanal makinenin yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="9f2e6-109">This command retrieves the configuration of a virtual machine named VirtualMachine12 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="9f2e6-110">Komut, ardışık düzen işlecini kullanarak bunu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="9f2e6-110">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9f2e6-111">Bu cmdlet bu sanal makinenin uç nokta bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="9f2e6-111">This cmdlet gets endpoint information for that virtual machine.</span></span>

## <span data-ttu-id="9f2e6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f2e6-112">PARAMETERS</span></span>

### <span data-ttu-id="9f2e6-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="9f2e6-113">-InformationAction</span></span>
<span data-ttu-id="9f2e6-114">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f2e6-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9f2e6-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9f2e6-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9f2e6-116">'A</span><span class="sxs-lookup"><span data-stu-id="9f2e6-116">Continue</span></span>
- <span data-ttu-id="9f2e6-117">Manıza</span><span class="sxs-lookup"><span data-stu-id="9f2e6-117">Ignore</span></span>
- <span data-ttu-id="9f2e6-118">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="9f2e6-118">Inquire</span></span>
- <span data-ttu-id="9f2e6-119">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="9f2e6-119">SilentlyContinue</span></span>
- <span data-ttu-id="9f2e6-120">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="9f2e6-120">Stop</span></span>
- <span data-ttu-id="9f2e6-121">Biliriz</span><span class="sxs-lookup"><span data-stu-id="9f2e6-121">Suspend</span></span>

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

### <span data-ttu-id="9f2e6-122">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="9f2e6-122">-InformationVariable</span></span>
<span data-ttu-id="9f2e6-123">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f2e6-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9f2e6-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="9f2e6-124">-Name</span></span>
<span data-ttu-id="9f2e6-125">Bu cmdlet 'in bilgi aldığı uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f2e6-125">Specifies the name of the endpoint for which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f2e6-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="9f2e6-126">-Profile</span></span>
<span data-ttu-id="9f2e6-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f2e6-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9f2e6-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="9f2e6-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9f2e6-129">-VM</span><span class="sxs-lookup"><span data-stu-id="9f2e6-129">-VM</span></span>
<span data-ttu-id="9f2e6-130">Bu cmdlet 'in uç nokta bilgilerini aldığı sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f2e6-130">Specifies the virtual machine from which this cmdlet gets endpoint information.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f2e6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f2e6-131">CommonParameters</span></span>
<span data-ttu-id="9f2e6-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f2e6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f2e6-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f2e6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f2e6-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f2e6-134">INPUTS</span></span>

## <span data-ttu-id="9f2e6-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f2e6-135">OUTPUTS</span></span>

## <span data-ttu-id="9f2e6-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f2e6-136">NOTES</span></span>

## <span data-ttu-id="9f2e6-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f2e6-137">RELATED LINKS</span></span>

[<span data-ttu-id="9f2e6-138">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f2e6-138">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="9f2e6-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="9f2e6-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="9f2e6-140">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f2e6-140">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="9f2e6-141">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f2e6-141">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)


