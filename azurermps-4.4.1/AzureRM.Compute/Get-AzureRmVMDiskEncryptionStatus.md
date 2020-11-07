---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
ms.openlocfilehash: 0d7312d7ecbddf15530438e9729e470bd202e488
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763400"
---
# <span data-ttu-id="c7a2c-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="c7a2c-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="c7a2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7a2c-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a2c-103">Sanal makinenin şifreleme durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="c7a2c-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7a2c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7a2c-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7a2c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7a2c-105">DESCRIPTION</span></span>
<span data-ttu-id="c7a2c-106">**Get-AzureRmVMDiskEncryptionStatus** cmdlet 'i sanal makinenin şifreleme durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="c7a2c-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="c7a2c-107">İşletim sisteminin ve veri birimlerinin şifreleme durumunu görüntüler.</span><span class="sxs-lookup"><span data-stu-id="c7a2c-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="c7a2c-108">Şifreleme durumuna ek olarak, şifreleme anahtarının ve işletim sistemi birimi için anahtar şifreleme **anahtarının bulunduğu tuş** durumlarının, anahtar şifreleme anahtarı URL 'sini, kaynak kimliklerini de görüntüler.</span><span class="sxs-lookup"><span data-stu-id="c7a2c-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="c7a2c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7a2c-109">EXAMPLES</span></span>

### <span data-ttu-id="c7a2c-110">Örnek 1: sanal makinenin şifreleme durumunu alma</span><span class="sxs-lookup"><span data-stu-id="c7a2c-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="c7a2c-111">Bu komut, VM001 adındaki sanal makinenin şifreleme durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="c7a2c-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="c7a2c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7a2c-112">PARAMETERS</span></span>

### <span data-ttu-id="c7a2c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a2c-113">-DefaultProfile</span></span>
<span data-ttu-id="c7a2c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c7a2c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7a2c-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="c7a2c-115">-Name</span></span>
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

### <span data-ttu-id="c7a2c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7a2c-116">-ResourceGroupName</span></span>
<span data-ttu-id="c7a2c-117">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a2c-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c7a2c-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="c7a2c-118">-VMName</span></span>
<span data-ttu-id="c7a2c-119">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a2c-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="c7a2c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a2c-120">CommonParameters</span></span>
<span data-ttu-id="c7a2c-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7a2c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a2c-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7a2c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a2c-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7a2c-123">INPUTS</span></span>

## <span data-ttu-id="c7a2c-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7a2c-124">OUTPUTS</span></span>

## <span data-ttu-id="c7a2c-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7a2c-125">NOTES</span></span>

## <span data-ttu-id="c7a2c-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7a2c-126">RELATED LINKS</span></span>

[<span data-ttu-id="c7a2c-127">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="c7a2c-127">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="c7a2c-128">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="c7a2c-128">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


