---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsswinrmlistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
ms.openlocfilehash: 00e61142948e42310dbd5c0be56660c17ec7e8e3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937074"
---
# <span data-ttu-id="47208-101">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="47208-101">Add-AzVmssWinRMListener</span></span>

## <span data-ttu-id="47208-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47208-102">SYNOPSIS</span></span>
<span data-ttu-id="47208-103">VMSS 'ye WinRM dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="47208-103">Adds a WinRM listener to the VMSS.</span></span>

## <span data-ttu-id="47208-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47208-104">SYNTAX</span></span>

```
Add-AzVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47208-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="47208-105">DESCRIPTION</span></span>
<span data-ttu-id="47208-106">**Add-AzVmssWinRMListener** cmdlet 'ı, sanal makine ölçek kümesinde (VMSS) Windows Uzaktan Yönetim (WinRM) dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="47208-106">The **Add-AzVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="47208-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47208-107">EXAMPLES</span></span>

### <span data-ttu-id="47208-108">Örnek 1: VMSS 'ye WinRM dinleyicisi ekleme</span><span class="sxs-lookup"><span data-stu-id="47208-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="47208-109">Bu örnek, VMSS 'ye bir WinRM dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="47208-109">This example adds a WinRM listener to the VMSS.</span></span>

<span data-ttu-id="47208-110">İlk komut, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="47208-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="47208-111">İkinci komut, belirtilen URL 'deki sertifikayı VMSS 'ye içeren bir HTTP protokolü WinRM dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="47208-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="47208-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47208-112">PARAMETERS</span></span>

### <span data-ttu-id="47208-113">-CertificateUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="47208-113">-CertificateUrl</span></span>
<span data-ttu-id="47208-114">Yeni sanal makinelerin sağlandığı sertifikanın URL 'sini içeren bir bağlantı belirtir.</span><span class="sxs-lookup"><span data-stu-id="47208-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

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

### <span data-ttu-id="47208-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47208-115">-DefaultProfile</span></span>
<span data-ttu-id="47208-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="47208-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47208-117">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="47208-117">-Protocol</span></span>
<span data-ttu-id="47208-118">WinRM dinleyicisi protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="47208-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="47208-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="47208-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="47208-120">Http</span><span class="sxs-lookup"><span data-stu-id="47208-120">Http</span></span>
- <span data-ttu-id="47208-121">Https</span><span class="sxs-lookup"><span data-stu-id="47208-121">Https</span></span>

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

### <span data-ttu-id="47208-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="47208-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="47208-123">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="47208-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="47208-124">Nesneyi oluşturmak için New-AzVmssConfig cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47208-124">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47208-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="47208-125">-Confirm</span></span>
<span data-ttu-id="47208-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="47208-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47208-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47208-127">-WhatIf</span></span>
<span data-ttu-id="47208-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47208-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47208-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="47208-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47208-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47208-130">CommonParameters</span></span>
<span data-ttu-id="47208-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47208-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47208-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47208-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47208-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47208-133">INPUTS</span></span>

### <span data-ttu-id="47208-134">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="47208-134">VirtualMachineScaleSet</span></span>
<span data-ttu-id="47208-135">' VirtualMachineScaleSet ' parametresi ardışık düzen için ' VirtualMachineScaleSet ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="47208-135">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="47208-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47208-136">OUTPUTS</span></span>

### <span data-ttu-id="47208-137">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="47208-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="47208-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47208-138">NOTES</span></span>

## <span data-ttu-id="47208-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47208-139">RELATED LINKS</span></span>

[<span data-ttu-id="47208-140">Yeni-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="47208-140">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


