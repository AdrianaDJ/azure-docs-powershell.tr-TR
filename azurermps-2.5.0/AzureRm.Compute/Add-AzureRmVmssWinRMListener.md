---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsswinrmlistener
schema: 2.0.0
ms.openlocfilehash: dd9c13298adac34a53ed2f97bbc1e3edc95892df
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939189"
---
# <span data-ttu-id="3a656-101">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="3a656-101">Add-AzureRmVmssWinRMListener</span></span>

## <span data-ttu-id="3a656-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a656-102">SYNOPSIS</span></span>
<span data-ttu-id="3a656-103">VMSS 'ye WinRM dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="3a656-103">Adds a WinRM listener to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a656-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a656-104">SYNTAX</span></span>

```
Add-AzureRmVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a656-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a656-105">DESCRIPTION</span></span>
<span data-ttu-id="3a656-106">**Add-AzureRmVmssWinRMListener** cmdlet 'ı, sanal makine ölçek kümesinde (VMSS) Windows Uzaktan Yönetim (WinRM) dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="3a656-106">The **Add-AzureRmVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="3a656-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a656-107">EXAMPLES</span></span>

### <span data-ttu-id="3a656-108">Örnek 1: VMSS 'ye WinRM dinleyicisi ekleme</span><span class="sxs-lookup"><span data-stu-id="3a656-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="3a656-109">Bu örnek, VMSS 'ye bir WinRM dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="3a656-109">This example adds a WinRM listener to the VMSS.</span></span>

<span data-ttu-id="3a656-110">İlk komut, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzureRmVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="3a656-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="3a656-111">İkinci komut, belirtilen URL 'deki sertifikayı VMSS 'ye içeren bir HTTP protokolü WinRM dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="3a656-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="3a656-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a656-112">PARAMETERS</span></span>

### <span data-ttu-id="3a656-113">-CertificateUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="3a656-113">-CertificateUrl</span></span>
<span data-ttu-id="3a656-114">Yeni sanal makinelerin sağlandığı sertifikanın URL 'sini içeren bir bağlantı belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a656-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

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

### <span data-ttu-id="3a656-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a656-115">-DefaultProfile</span></span>
<span data-ttu-id="3a656-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3a656-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a656-117">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="3a656-117">-Protocol</span></span>
<span data-ttu-id="3a656-118">WinRM dinleyicisi protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a656-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="3a656-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3a656-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3a656-120">Http</span><span class="sxs-lookup"><span data-stu-id="3a656-120">Http</span></span>
- <span data-ttu-id="3a656-121">Https</span><span class="sxs-lookup"><span data-stu-id="3a656-121">Https</span></span>

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

### <span data-ttu-id="3a656-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3a656-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3a656-123">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a656-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="3a656-124">Nesneyi oluşturmak için New-AzureRmVmssConfig cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3a656-124">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="3a656-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="3a656-125">-Confirm</span></span>
<span data-ttu-id="3a656-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3a656-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a656-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a656-127">-WhatIf</span></span>
<span data-ttu-id="3a656-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a656-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a656-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3a656-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a656-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a656-130">CommonParameters</span></span>
<span data-ttu-id="3a656-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a656-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a656-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a656-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a656-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a656-133">INPUTS</span></span>

### <span data-ttu-id="3a656-134">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3a656-134">VirtualMachineScaleSet</span></span>
<span data-ttu-id="3a656-135">' VirtualMachineScaleSet ' parametresi ardışık düzen için ' VirtualMachineScaleSet ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3a656-135">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="3a656-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a656-136">OUTPUTS</span></span>

### <span data-ttu-id="3a656-137">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="3a656-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="3a656-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a656-138">NOTES</span></span>

## <span data-ttu-id="3a656-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a656-139">RELATED LINKS</span></span>

[<span data-ttu-id="3a656-140">Yeni-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="3a656-140">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


