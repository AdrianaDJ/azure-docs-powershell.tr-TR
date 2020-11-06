---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
ms.openlocfilehash: 9ec94d0c11bf9302156355c28566ce16f48ae148
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590519"
---
# <span data-ttu-id="8b8c2-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="8b8c2-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="8b8c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b8c2-102">SYNOPSIS</span></span>
<span data-ttu-id="8b8c2-103">Sanal makinenin şifreleme durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="8b8c2-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b8c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b8c2-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b8c2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b8c2-105">DESCRIPTION</span></span>
<span data-ttu-id="8b8c2-106">**Get-AzureRmVMDiskEncryptionStatus** cmdlet 'i sanal makinenin şifreleme durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="8b8c2-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="8b8c2-107">İşletim sisteminin ve veri birimlerinin şifreleme durumunu görüntüler.</span><span class="sxs-lookup"><span data-stu-id="8b8c2-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="8b8c2-108">Şifreleme durumuna ek olarak, şifreleme anahtarının ve işletim sistemi birimi için anahtar şifreleme **anahtarının bulunduğu tuş** durumlarının, anahtar şifreleme anahtarı URL 'sini, kaynak kimliklerini de görüntüler.</span><span class="sxs-lookup"><span data-stu-id="8b8c2-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="8b8c2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b8c2-109">EXAMPLES</span></span>

### <span data-ttu-id="8b8c2-110">Örnek 1: sanal makinenin şifreleme durumunu alma</span><span class="sxs-lookup"><span data-stu-id="8b8c2-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="8b8c2-111">Bu komut, VM001 adındaki sanal makinenin şifreleme durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="8b8c2-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="8b8c2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b8c2-112">PARAMETERS</span></span>

### <span data-ttu-id="8b8c2-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="8b8c2-113">-Name</span></span>
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

### <span data-ttu-id="8b8c2-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b8c2-114">-ResourceGroupName</span></span>
<span data-ttu-id="8b8c2-115">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b8c2-115">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8b8c2-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="8b8c2-116">-VMName</span></span>
<span data-ttu-id="8b8c2-117">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b8c2-117">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="8b8c2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b8c2-118">CommonParameters</span></span>
<span data-ttu-id="8b8c2-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b8c2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b8c2-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b8c2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b8c2-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b8c2-121">INPUTS</span></span>

### <span data-ttu-id="8b8c2-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8b8c2-122">None</span></span>
<span data-ttu-id="8b8c2-123">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="8b8c2-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8b8c2-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b8c2-124">OUTPUTS</span></span>

## <span data-ttu-id="8b8c2-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b8c2-125">NOTES</span></span>

## <span data-ttu-id="8b8c2-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b8c2-126">RELATED LINKS</span></span>

[<span data-ttu-id="8b8c2-127">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="8b8c2-127">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="8b8c2-128">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="8b8c2-128">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


