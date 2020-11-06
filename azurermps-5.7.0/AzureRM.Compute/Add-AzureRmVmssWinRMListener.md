---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
ms.openlocfilehash: d2ed576131ad2ff33ae7e5c7e5be091ca8f4a50e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586809"
---
# <span data-ttu-id="e32f8-101">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="e32f8-101">Add-AzureRmVmssWinRMListener</span></span>

## <span data-ttu-id="e32f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e32f8-102">SYNOPSIS</span></span>
<span data-ttu-id="e32f8-103">VMSS 'ye WinRM dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="e32f8-103">Adds a WinRM listener to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e32f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e32f8-104">SYNTAX</span></span>

```
Add-AzureRmVmssWinRMListener [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e32f8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e32f8-105">DESCRIPTION</span></span>
<span data-ttu-id="e32f8-106">**Add-AzureRmVmssWinRMListener** cmdlet 'ı, sanal makine ölçek kümesinde (VMSS) Windows Uzaktan Yönetim (WinRM) dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="e32f8-106">The **Add-AzureRmVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="e32f8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e32f8-107">EXAMPLES</span></span>

### <span data-ttu-id="e32f8-108">Örnek 1: VMSS 'ye WinRM dinleyicisi ekleme</span><span class="sxs-lookup"><span data-stu-id="e32f8-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="e32f8-109">Bu örnek, VMSS 'ye bir WinRM dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="e32f8-109">This example adds a WinRM listener to the VMSS.</span></span>

<span data-ttu-id="e32f8-110">İlk komut, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzureRmVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="e32f8-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="e32f8-111">İkinci komut, belirtilen URL 'deki sertifikayı VMSS 'ye içeren bir HTTP protokolü WinRM dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="e32f8-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="e32f8-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e32f8-112">PARAMETERS</span></span>

### <span data-ttu-id="e32f8-113">-CertificateUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="e32f8-113">-CertificateUrl</span></span>
<span data-ttu-id="e32f8-114">Yeni sanal makinelerin sağlandığı sertifikanın URL 'sini içeren bir bağlantı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e32f8-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e32f8-115">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="e32f8-115">-Protocol</span></span>
<span data-ttu-id="e32f8-116">WinRM dinleyicisi protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e32f8-116">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="e32f8-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e32f8-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e32f8-118">Http</span><span class="sxs-lookup"><span data-stu-id="e32f8-118">Http</span></span>
- <span data-ttu-id="e32f8-119">Https</span><span class="sxs-lookup"><span data-stu-id="e32f8-119">Https</span></span>

```yaml
Type: ProtocolTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e32f8-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e32f8-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e32f8-121">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e32f8-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="e32f8-122">Nesneyi oluşturmak için New-AzureRmVmssConfig cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e32f8-122">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e32f8-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="e32f8-123">-Confirm</span></span>
<span data-ttu-id="e32f8-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e32f8-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e32f8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e32f8-125">-WhatIf</span></span>
<span data-ttu-id="e32f8-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e32f8-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e32f8-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e32f8-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e32f8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e32f8-128">CommonParameters</span></span>
<span data-ttu-id="e32f8-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e32f8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e32f8-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e32f8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e32f8-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e32f8-131">INPUTS</span></span>

### <span data-ttu-id="e32f8-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e32f8-132">None</span></span>
<span data-ttu-id="e32f8-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e32f8-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e32f8-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e32f8-134">OUTPUTS</span></span>

### <span data-ttu-id="e32f8-135">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="e32f8-135">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="e32f8-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e32f8-136">NOTES</span></span>

## <span data-ttu-id="e32f8-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e32f8-137">RELATED LINKS</span></span>

[<span data-ttu-id="e32f8-138">Yeni-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e32f8-138">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


