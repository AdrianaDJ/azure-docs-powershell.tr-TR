---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: 809246520c4e6b07a1aca406ef3ec17eb9df31f1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937039"
---
# <span data-ttu-id="c29b1-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="c29b1-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="c29b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c29b1-102">SYNOPSIS</span></span>
<span data-ttu-id="c29b1-103">AD etki alanı uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c29b1-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="c29b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c29b1-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c29b1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c29b1-105">DESCRIPTION</span></span>
<span data-ttu-id="c29b1-106">**Get-AzVMADDomainExtension** cmdlet 'ı belirtilen Azure Active DIRECTORY (ad) etki alanı uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c29b1-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="c29b1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c29b1-107">EXAMPLES</span></span>

### <span data-ttu-id="c29b1-108">2</span><span class="sxs-lookup"><span data-stu-id="c29b1-108">1:</span></span>
```

```

## <span data-ttu-id="c29b1-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c29b1-109">PARAMETERS</span></span>

### <span data-ttu-id="c29b1-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c29b1-110">-DefaultProfile</span></span>
<span data-ttu-id="c29b1-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c29b1-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c29b1-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="c29b1-112">-Name</span></span>
<span data-ttu-id="c29b1-113">Etki alanı uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c29b1-113">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="c29b1-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c29b1-114">-ResourceGroupName</span></span>
<span data-ttu-id="c29b1-115">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c29b1-115">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c29b1-116">-Durum</span><span class="sxs-lookup"><span data-stu-id="c29b1-116">-Status</span></span>
<span data-ttu-id="c29b1-117">Bu cmdlet 'in etki alanı uzantısının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c29b1-117">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="c29b1-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="c29b1-118">-VMName</span></span>
<span data-ttu-id="c29b1-119">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c29b1-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="c29b1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c29b1-120">CommonParameters</span></span>
<span data-ttu-id="c29b1-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c29b1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c29b1-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c29b1-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c29b1-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c29b1-123">INPUTS</span></span>

### <span data-ttu-id="c29b1-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c29b1-124">None</span></span>
<span data-ttu-id="c29b1-125">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c29b1-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c29b1-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c29b1-126">OUTPUTS</span></span>

### <span data-ttu-id="c29b1-127">Microsoft. Azure. Commands. COMPUTE. modeller. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="c29b1-127">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="c29b1-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c29b1-128">NOTES</span></span>

## <span data-ttu-id="c29b1-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c29b1-129">RELATED LINKS</span></span>

[<span data-ttu-id="c29b1-130">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="c29b1-130">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)


