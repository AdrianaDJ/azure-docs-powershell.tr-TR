---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaddomainextension
schema: 2.0.0
ms.openlocfilehash: 01a5a69053cfd05186abae45d5b53fff0b022b98
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939173"
---
# <span data-ttu-id="64f91-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="64f91-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="64f91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64f91-102">SYNOPSIS</span></span>
<span data-ttu-id="64f91-103">AD etki alanı uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="64f91-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64f91-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="64f91-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64f91-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="64f91-105">DESCRIPTION</span></span>
<span data-ttu-id="64f91-106">**Get-AzureRmVMADDomainExtension** cmdlet 'ı belirtilen Azure Active DIRECTORY (ad) etki alanı uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="64f91-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="64f91-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="64f91-107">EXAMPLES</span></span>

### <span data-ttu-id="64f91-108">2</span><span class="sxs-lookup"><span data-stu-id="64f91-108">1:</span></span>
```

```

## <span data-ttu-id="64f91-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="64f91-109">PARAMETERS</span></span>

### <span data-ttu-id="64f91-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64f91-110">-DefaultProfile</span></span>
<span data-ttu-id="64f91-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="64f91-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64f91-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="64f91-112">-Name</span></span>
<span data-ttu-id="64f91-113">Etki alanı uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64f91-113">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="64f91-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64f91-114">-ResourceGroupName</span></span>
<span data-ttu-id="64f91-115">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64f91-115">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="64f91-116">-Durum</span><span class="sxs-lookup"><span data-stu-id="64f91-116">-Status</span></span>
<span data-ttu-id="64f91-117">Bu cmdlet 'in etki alanı uzantısının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="64f91-117">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="64f91-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="64f91-118">-VMName</span></span>
<span data-ttu-id="64f91-119">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64f91-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="64f91-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64f91-120">CommonParameters</span></span>
<span data-ttu-id="64f91-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="64f91-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64f91-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64f91-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64f91-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="64f91-123">INPUTS</span></span>

### <span data-ttu-id="64f91-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="64f91-124">None</span></span>
<span data-ttu-id="64f91-125">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="64f91-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="64f91-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="64f91-126">OUTPUTS</span></span>

### <span data-ttu-id="64f91-127">Microsoft. Azure. Commands. COMPUTE. modeller. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="64f91-127">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="64f91-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="64f91-128">NOTES</span></span>

## <span data-ttu-id="64f91-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="64f91-129">RELATED LINKS</span></span>

[<span data-ttu-id="64f91-130">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="64f91-130">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


