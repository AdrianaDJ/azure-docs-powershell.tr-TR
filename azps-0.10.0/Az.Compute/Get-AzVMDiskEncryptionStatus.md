---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 30c8b79d3951f0d557704bc3d0c0ac4919fccac1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937026"
---
# <span data-ttu-id="2a95e-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="2a95e-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="2a95e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a95e-102">SYNOPSIS</span></span>
<span data-ttu-id="2a95e-103">Sanal makinenin şifreleme durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="2a95e-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="2a95e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a95e-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a95e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a95e-105">DESCRIPTION</span></span>
<span data-ttu-id="2a95e-106">**Get-AzVMDiskEncryptionStatus** cmdlet 'i sanal makinenin şifreleme durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="2a95e-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="2a95e-107">İşletim sisteminin ve veri birimlerinin şifreleme durumunu görüntüler.</span><span class="sxs-lookup"><span data-stu-id="2a95e-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="2a95e-108">Şifreleme durumuna ek olarak, şifreleme anahtarının ve işletim sistemi birimi için anahtar şifreleme **anahtarının bulunduğu tuş** durumlarının, anahtar şifreleme anahtarı URL 'sini, kaynak kimliklerini de görüntüler.</span><span class="sxs-lookup"><span data-stu-id="2a95e-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="2a95e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a95e-109">EXAMPLES</span></span>

### <span data-ttu-id="2a95e-110">Örnek 1: sanal makinenin şifreleme durumunu alma</span><span class="sxs-lookup"><span data-stu-id="2a95e-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="2a95e-111">Bu komut, VM001 adındaki sanal makinenin şifreleme durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="2a95e-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="2a95e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a95e-112">PARAMETERS</span></span>

### <span data-ttu-id="2a95e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a95e-113">-DefaultProfile</span></span>
<span data-ttu-id="2a95e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2a95e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a95e-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="2a95e-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="2a95e-116">Dahili yayımcı adı.</span><span class="sxs-lookup"><span data-stu-id="2a95e-116">The extension publisher name.</span></span> <span data-ttu-id="2a95e-117">Bu parametreyi yalnızca "Microsoft. Azure. Security" varsayılan değerini geçersiz kılmak için belirtin.</span><span class="sxs-lookup"><span data-stu-id="2a95e-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a95e-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="2a95e-118">-ExtensionType</span></span>
<span data-ttu-id="2a95e-119">Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="2a95e-119">The extension type.</span></span> <span data-ttu-id="2a95e-120">Windows VM 'ler için "AzureDiskEncryption" varsayılan değerini (Linux VM 'Ler için "AzureDiskEncryptionForLinux" olarak geçersiz kılmak için bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="2a95e-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a95e-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="2a95e-121">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a95e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a95e-122">-ResourceGroupName</span></span>
<span data-ttu-id="2a95e-123">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a95e-123">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a95e-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="2a95e-124">-VMName</span></span>
<span data-ttu-id="2a95e-125">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a95e-125">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a95e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a95e-126">CommonParameters</span></span>
<span data-ttu-id="2a95e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a95e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a95e-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a95e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a95e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a95e-129">INPUTS</span></span>

### <span data-ttu-id="2a95e-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2a95e-130">None</span></span>
<span data-ttu-id="2a95e-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="2a95e-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2a95e-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a95e-132">OUTPUTS</span></span>

### <span data-ttu-id="2a95e-133">Microsoft. Azure. Commands. COMPUTE. Extension. AzureDiskEncryption. AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="2a95e-133">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="2a95e-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a95e-134">NOTES</span></span>

## <span data-ttu-id="2a95e-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a95e-135">RELATED LINKS</span></span>

[<span data-ttu-id="2a95e-136">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="2a95e-136">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="2a95e-137">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="2a95e-137">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


