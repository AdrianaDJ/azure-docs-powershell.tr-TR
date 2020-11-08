---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 4ad5ef08f9c12693a2fa4b4b372ee1320f90fb76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108427"
---
# <span data-ttu-id="af19d-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="af19d-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="af19d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af19d-102">SYNOPSIS</span></span>
<span data-ttu-id="af19d-103">Sanal makinenin şifreleme durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="af19d-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="af19d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af19d-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af19d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="af19d-105">DESCRIPTION</span></span>
<span data-ttu-id="af19d-106">**Get-AzVMDiskEncryptionStatus** cmdlet 'i sanal makinenin şifreleme durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="af19d-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="af19d-107">İşletim sisteminin ve veri birimlerinin şifreleme durumunu görüntüler.</span><span class="sxs-lookup"><span data-stu-id="af19d-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="af19d-108">Şifreleme durumuna ek olarak, şifreleme anahtarının ve işletim sistemi birimi için anahtar şifreleme **anahtarının bulunduğu tuş** durumlarının, anahtar şifreleme anahtarı URL 'sini, kaynak kimliklerini de görüntüler.</span><span class="sxs-lookup"><span data-stu-id="af19d-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="af19d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af19d-109">EXAMPLES</span></span>

### <span data-ttu-id="af19d-110">Örnek 1: sanal makinenin şifreleme durumunu alma</span><span class="sxs-lookup"><span data-stu-id="af19d-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="af19d-111">Bu komut, VM001 adındaki sanal makinenin şifreleme durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="af19d-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="af19d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af19d-112">PARAMETERS</span></span>

### <span data-ttu-id="af19d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af19d-113">-DefaultProfile</span></span>
<span data-ttu-id="af19d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af19d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af19d-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="af19d-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="af19d-116">Dahili yayımcı adı.</span><span class="sxs-lookup"><span data-stu-id="af19d-116">The extension publisher name.</span></span> <span data-ttu-id="af19d-117">Bu parametreyi yalnızca "Microsoft. Azure. Security" varsayılan değerini geçersiz kılmak için belirtin.</span><span class="sxs-lookup"><span data-stu-id="af19d-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af19d-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="af19d-118">-ExtensionType</span></span>
<span data-ttu-id="af19d-119">Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="af19d-119">The extension type.</span></span> <span data-ttu-id="af19d-120">Windows VM 'ler için "AzureDiskEncryption" varsayılan değerini (Linux VM 'Ler için "AzureDiskEncryptionForLinux" olarak geçersiz kılmak için bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="af19d-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af19d-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="af19d-121">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af19d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af19d-122">-ResourceGroupName</span></span>
<span data-ttu-id="af19d-123">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af19d-123">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af19d-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="af19d-124">-VMName</span></span>
<span data-ttu-id="af19d-125">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af19d-125">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af19d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af19d-126">CommonParameters</span></span>
<span data-ttu-id="af19d-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af19d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af19d-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="af19d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af19d-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af19d-129">INPUTS</span></span>

### <span data-ttu-id="af19d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="af19d-130">System.String</span></span>

## <span data-ttu-id="af19d-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af19d-131">OUTPUTS</span></span>

### <span data-ttu-id="af19d-132">Microsoft. Azure. Commands. COMPUTE. Extension. AzureDiskEncryption. AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="af19d-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="af19d-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af19d-133">NOTES</span></span>

## <span data-ttu-id="af19d-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af19d-134">RELATED LINKS</span></span>

[<span data-ttu-id="af19d-135">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="af19d-135">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="af19d-136">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="af19d-136">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


