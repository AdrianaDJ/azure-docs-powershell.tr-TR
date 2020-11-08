---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0A32348E-C38D-4555-8F7C-6515F4EE7F23
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc1c469d35f4cc281fa22252e7e81509be06761
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105673"
---
# <span data-ttu-id="853d3-101">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="853d3-101">Get-AzureAclConfig</span></span>

## <span data-ttu-id="853d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="853d3-102">SYNOPSIS</span></span>
<span data-ttu-id="853d3-103">Bir Azure sanal makinesinden ACL yapılandırma nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="853d3-103">Gets the ACL configuration object from an Azure virtual machine.</span></span>

## <span data-ttu-id="853d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="853d3-104">SYNTAX</span></span>

```
Get-AzureAclConfig [[-EndpointName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="853d3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="853d3-105">DESCRIPTION</span></span>
<span data-ttu-id="853d3-106">**Get-AzureAclConfig** cmdlet 'i mevcut bir Azure sanal makinesinden erişim denetim LISTESI (ACL) yapılandırma nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="853d3-106">The **Get-AzureAclConfig** cmdlet gets the access control list (ACL) configuration object from an existing Azure virtual machine.</span></span>

## <span data-ttu-id="853d3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="853d3-107">EXAMPLES</span></span>

### <span data-ttu-id="853d3-108">Örnek 1: sanal makine uç noktası için ACL yapılandırma nesnesi alma</span><span class="sxs-lookup"><span data-stu-id="853d3-108">Example 1: Get an ACL configuration object for a virtual machine endpoint</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
```

<span data-ttu-id="853d3-109">İlk komut, VirtualMachine07 adındaki sanal makineyi, **Get-AzureVM** cmdlet 'Ini kullanarak contososervice adındaki hizmette alır.</span><span class="sxs-lookup"><span data-stu-id="853d3-109">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="853d3-110">Komut, bu nesneyi ardışık düzen işlecini kullanarak **Get-AzureAclConfig** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="853d3-110">The command passes that object to the **Get-AzureAclConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="853d3-111">Bu cmdlet Web adlı uç noktanın ACL yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="853d3-111">That cmdlet gets the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="853d3-112">Komut bu ACL yapılandırma nesnesini $Acl değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="853d3-112">The command stores that ACL configuration object in the $Acl variable.</span></span>

## <span data-ttu-id="853d3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="853d3-113">PARAMETERS</span></span>

### <span data-ttu-id="853d3-114">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="853d3-114">-EndpointName</span></span>
<span data-ttu-id="853d3-115">Bu cmdlet 'in ACL aldığı uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="853d3-115">Specifies the name of the endpoint for which this cmdlet gets an ACL.</span></span>

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

### <span data-ttu-id="853d3-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="853d3-116">-InformationAction</span></span>
<span data-ttu-id="853d3-117">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="853d3-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="853d3-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="853d3-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="853d3-119">'A</span><span class="sxs-lookup"><span data-stu-id="853d3-119">Continue</span></span>
- <span data-ttu-id="853d3-120">Manıza</span><span class="sxs-lookup"><span data-stu-id="853d3-120">Ignore</span></span>
- <span data-ttu-id="853d3-121">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="853d3-121">Inquire</span></span>
- <span data-ttu-id="853d3-122">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="853d3-122">SilentlyContinue</span></span>
- <span data-ttu-id="853d3-123">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="853d3-123">Stop</span></span>
- <span data-ttu-id="853d3-124">Biliriz</span><span class="sxs-lookup"><span data-stu-id="853d3-124">Suspend</span></span>

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

### <span data-ttu-id="853d3-125">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="853d3-125">-InformationVariable</span></span>
<span data-ttu-id="853d3-126">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="853d3-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="853d3-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="853d3-127">-Profile</span></span>
<span data-ttu-id="853d3-128">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="853d3-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="853d3-129">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="853d3-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="853d3-130">-VM</span><span class="sxs-lookup"><span data-stu-id="853d3-130">-VM</span></span>
<span data-ttu-id="853d3-131">Bu cmdlet 'in ACL yapılandırmasını aldığı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="853d3-131">Specifies the virtual machine object for which this cmdlet gets ACL configuration.</span></span>

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

### <span data-ttu-id="853d3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="853d3-132">CommonParameters</span></span>
<span data-ttu-id="853d3-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="853d3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="853d3-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="853d3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="853d3-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="853d3-135">INPUTS</span></span>

## <span data-ttu-id="853d3-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="853d3-136">OUTPUTS</span></span>

## <span data-ttu-id="853d3-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="853d3-137">NOTES</span></span>

## <span data-ttu-id="853d3-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="853d3-138">RELATED LINKS</span></span>

[<span data-ttu-id="853d3-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="853d3-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="853d3-140">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="853d3-140">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="853d3-141">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="853d3-141">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="853d3-142">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="853d3-142">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)


