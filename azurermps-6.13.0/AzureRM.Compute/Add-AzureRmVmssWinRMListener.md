---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsswinrmlistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
ms.openlocfilehash: 23da9524d2641f390fcd29a62fd469d34cf05de3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591368"
---
# <span data-ttu-id="b4286-101">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="b4286-101">Add-AzureRmVmssWinRMListener</span></span>

## <span data-ttu-id="b4286-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4286-102">SYNOPSIS</span></span>
<span data-ttu-id="b4286-103">VMSS 'ye WinRM dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="b4286-103">Adds a WinRM listener to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4286-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4286-104">SYNTAX</span></span>

```
Add-AzureRmVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4286-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4286-105">DESCRIPTION</span></span>
<span data-ttu-id="b4286-106">**Add-AzureRmVmssWinRMListener** cmdlet 'ı, sanal makine ölçek kümesinde (VMSS) Windows Uzaktan Yönetim (WinRM) dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="b4286-106">The **Add-AzureRmVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="b4286-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4286-107">EXAMPLES</span></span>

### <span data-ttu-id="b4286-108">Örnek 1: VMSS 'ye WinRM dinleyicisi ekleme</span><span class="sxs-lookup"><span data-stu-id="b4286-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="b4286-109">Bu örnek, VMSS 'ye bir WinRM dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="b4286-109">This example adds a WinRM listener to the VMSS.</span></span>
<span data-ttu-id="b4286-110">İlk komut, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzureRmVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="b4286-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="b4286-111">İkinci komut, belirtilen URL 'deki sertifikayı VMSS 'ye içeren bir HTTP protokolü WinRM dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="b4286-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="b4286-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4286-112">PARAMETERS</span></span>

### <span data-ttu-id="b4286-113">-CertificateUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="b4286-113">-CertificateUrl</span></span>
<span data-ttu-id="b4286-114">Yeni sanal makinelerin sağlandığı sertifikanın URL 'sini içeren bir bağlantı belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4286-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4286-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4286-115">-DefaultProfile</span></span>
<span data-ttu-id="b4286-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4286-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4286-117">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="b4286-117">-Protocol</span></span>
<span data-ttu-id="b4286-118">WinRM dinleyicisi protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4286-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="b4286-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b4286-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b4286-120">Http</span><span class="sxs-lookup"><span data-stu-id="b4286-120">Http</span></span>
- <span data-ttu-id="b4286-121">Https</span><span class="sxs-lookup"><span data-stu-id="b4286-121">Https</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ProtocolTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4286-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b4286-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b4286-123">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4286-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="b4286-124">Nesneyi oluşturmak için New-AzureRmVmssConfig cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b4286-124">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4286-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="b4286-125">-Confirm</span></span>
<span data-ttu-id="b4286-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b4286-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4286-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4286-127">-WhatIf</span></span>
<span data-ttu-id="b4286-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4286-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4286-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b4286-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4286-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4286-130">CommonParameters</span></span>
<span data-ttu-id="b4286-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4286-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4286-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4286-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4286-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4286-133">INPUTS</span></span>

### <span data-ttu-id="b4286-134">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b4286-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="b4286-135">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. ProtocolTypes, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b4286-135">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b4286-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b4286-136">System.String</span></span>

## <span data-ttu-id="b4286-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4286-137">OUTPUTS</span></span>

### <span data-ttu-id="b4286-138">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b4286-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="b4286-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4286-139">NOTES</span></span>

## <span data-ttu-id="b4286-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4286-140">RELATED LINKS</span></span>

[<span data-ttu-id="b4286-141">Yeni-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="b4286-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


