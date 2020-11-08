---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5A068EC9-3745-4219-BA03-C56CB9D9D157
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24fad9fc499c3f7abec5e7539fd1e221835849ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106478"
---
# <span data-ttu-id="44b15-101">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="44b15-101">Remove-AzureEndpoint</span></span>

## <span data-ttu-id="44b15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44b15-102">SYNOPSIS</span></span>
<span data-ttu-id="44b15-103">Bir Azure sanal makinesinden uç nokta siler.</span><span class="sxs-lookup"><span data-stu-id="44b15-103">Deletes an endpoint from an Azure virtual machine.</span></span>

## <span data-ttu-id="44b15-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="44b15-104">SYNTAX</span></span>

```
Remove-AzureEndpoint [-Name] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="44b15-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="44b15-105">DESCRIPTION</span></span>
<span data-ttu-id="44b15-106">**Remove-AzureEndpoint** cmdlet 'i Azure sanal makine nesnesinden bir uç noktayı siler.</span><span class="sxs-lookup"><span data-stu-id="44b15-106">The **Remove-AzureEndpoint** cmdlet deletes an endpoint from an Azure virtual machine object.</span></span>

## <span data-ttu-id="44b15-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="44b15-107">EXAMPLES</span></span>

### <span data-ttu-id="44b15-108">Örnek 1: uç noktayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="44b15-108">Example 1: Remove an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine01" | Remove-AzureEndpoint -Name "HttpIn" | Update-AzureVM
```

<span data-ttu-id="44b15-109">Bu komut, **Get-AzureVM** cmdlet 'Ini kullanarak VirtualMachine01 adındaki sanal makinenin yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="44b15-109">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="44b15-110">Komut, ardışık düzen işlecini kullanarak bunu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="44b15-110">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="44b15-111">Bu cmdlet, HttpIn adındaki uç noktayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="44b15-111">This cmdlet removes an endpoint named HttpIn.</span></span>
<span data-ttu-id="44b15-112">Komut, sanal makine nesnesini, değişikliklerinizi uygulayan **Update-AzureVM** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="44b15-112">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="44b15-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="44b15-113">PARAMETERS</span></span>

### <span data-ttu-id="44b15-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="44b15-114">-InformationAction</span></span>
<span data-ttu-id="44b15-115">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="44b15-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="44b15-116">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="44b15-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="44b15-117">'A</span><span class="sxs-lookup"><span data-stu-id="44b15-117">Continue</span></span>
- <span data-ttu-id="44b15-118">Manıza</span><span class="sxs-lookup"><span data-stu-id="44b15-118">Ignore</span></span>
- <span data-ttu-id="44b15-119">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="44b15-119">Inquire</span></span>
- <span data-ttu-id="44b15-120">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="44b15-120">SilentlyContinue</span></span>
- <span data-ttu-id="44b15-121">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="44b15-121">Stop</span></span>
- <span data-ttu-id="44b15-122">Biliriz</span><span class="sxs-lookup"><span data-stu-id="44b15-122">Suspend</span></span>

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

### <span data-ttu-id="44b15-123">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="44b15-123">-InformationVariable</span></span>
<span data-ttu-id="44b15-124">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="44b15-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="44b15-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="44b15-125">-Name</span></span>
<span data-ttu-id="44b15-126">Bu cmdlet 'in sanal makineden sildiği uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="44b15-126">Specifies the name of the endpoint that this cmdlet deletes from the virtual machine.</span></span>

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

### <span data-ttu-id="44b15-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="44b15-127">-Profile</span></span>
<span data-ttu-id="44b15-128">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="44b15-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="44b15-129">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="44b15-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="44b15-130">-VM</span><span class="sxs-lookup"><span data-stu-id="44b15-130">-VM</span></span>
<span data-ttu-id="44b15-131">Bu cmdlet 'in uç noktayı sildiği sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="44b15-131">Specifies the virtual machine from which this cmdlet deletes an endpoint.</span></span>

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

### <span data-ttu-id="44b15-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44b15-132">CommonParameters</span></span>
<span data-ttu-id="44b15-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="44b15-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44b15-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44b15-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44b15-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="44b15-135">INPUTS</span></span>

## <span data-ttu-id="44b15-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="44b15-136">OUTPUTS</span></span>

## <span data-ttu-id="44b15-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="44b15-137">NOTES</span></span>

## <span data-ttu-id="44b15-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="44b15-138">RELATED LINKS</span></span>

[<span data-ttu-id="44b15-139">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="44b15-139">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="44b15-140">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="44b15-140">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="44b15-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="44b15-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="44b15-142">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="44b15-142">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="44b15-143">Güncelleştirme-AzureVM</span><span class="sxs-lookup"><span data-stu-id="44b15-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


