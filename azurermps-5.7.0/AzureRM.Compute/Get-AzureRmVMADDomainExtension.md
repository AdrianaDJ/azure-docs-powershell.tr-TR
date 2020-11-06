---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
ms.openlocfilehash: d55d84560ca75a508a05276d8d33eb78d1d50ab5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591063"
---
# <span data-ttu-id="7a1f6-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="7a1f6-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="7a1f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a1f6-102">SYNOPSIS</span></span>
<span data-ttu-id="7a1f6-103">AD etki alanı uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="7a1f6-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a1f6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7a1f6-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="7a1f6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7a1f6-105">DESCRIPTION</span></span>
<span data-ttu-id="7a1f6-106">**Get-AzureRmVMADDomainExtension** cmdlet 'ı belirtilen Azure Active DIRECTORY (ad) etki alanı uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="7a1f6-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="7a1f6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7a1f6-107">EXAMPLES</span></span>

## <span data-ttu-id="7a1f6-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7a1f6-108">PARAMETERS</span></span>

### <span data-ttu-id="7a1f6-109">-Ad</span><span class="sxs-lookup"><span data-stu-id="7a1f6-109">-Name</span></span>
<span data-ttu-id="7a1f6-110">Etki alanı uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a1f6-110">Specifies the name of the domain extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a1f6-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a1f6-111">-ResourceGroupName</span></span>
<span data-ttu-id="7a1f6-112">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a1f6-112">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7a1f6-113">-Durum</span><span class="sxs-lookup"><span data-stu-id="7a1f6-113">-Status</span></span>
<span data-ttu-id="7a1f6-114">Bu cmdlet 'in etki alanı uzantısının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7a1f6-114">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a1f6-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="7a1f6-115">-VMName</span></span>
<span data-ttu-id="7a1f6-116">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a1f6-116">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="7a1f6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a1f6-117">CommonParameters</span></span>
<span data-ttu-id="7a1f6-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7a1f6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a1f6-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a1f6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a1f6-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7a1f6-120">INPUTS</span></span>

### <span data-ttu-id="7a1f6-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7a1f6-121">None</span></span>
<span data-ttu-id="7a1f6-122">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="7a1f6-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7a1f6-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7a1f6-123">OUTPUTS</span></span>

## <span data-ttu-id="7a1f6-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7a1f6-124">NOTES</span></span>

## <span data-ttu-id="7a1f6-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7a1f6-125">RELATED LINKS</span></span>

[<span data-ttu-id="7a1f6-126">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="7a1f6-126">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


