---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: ca6b3d4863629aa94585db9850042fff4165dd10
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94105066"
---
# <span data-ttu-id="be240-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="be240-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="be240-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be240-102">SYNOPSIS</span></span>
<span data-ttu-id="be240-103">AD etki alanı uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="be240-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="be240-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be240-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be240-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="be240-105">DESCRIPTION</span></span>
<span data-ttu-id="be240-106">**Get-AzVMADDomainExtension** cmdlet 'ı belirtilen Azure Active DIRECTORY (ad) etki alanı uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="be240-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="be240-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be240-107">EXAMPLES</span></span>

## <span data-ttu-id="be240-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be240-108">PARAMETERS</span></span>

### <span data-ttu-id="be240-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be240-109">-DefaultProfile</span></span>
<span data-ttu-id="be240-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="be240-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be240-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="be240-111">-Name</span></span>
<span data-ttu-id="be240-112">Etki alanı uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be240-112">Specifies the name of the domain extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be240-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be240-113">-ResourceGroupName</span></span>
<span data-ttu-id="be240-114">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be240-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="be240-115">-Durum</span><span class="sxs-lookup"><span data-stu-id="be240-115">-Status</span></span>
<span data-ttu-id="be240-116">Bu cmdlet 'in etki alanı uzantısının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="be240-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be240-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="be240-117">-VMName</span></span>
<span data-ttu-id="be240-118">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be240-118">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="be240-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be240-119">CommonParameters</span></span>
<span data-ttu-id="be240-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be240-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be240-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="be240-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be240-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be240-122">INPUTS</span></span>

### <span data-ttu-id="be240-123">System. String</span><span class="sxs-lookup"><span data-stu-id="be240-123">System.String</span></span>

### <span data-ttu-id="be240-124">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="be240-124">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="be240-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be240-125">OUTPUTS</span></span>

### <span data-ttu-id="be240-126">Microsoft. Azure. Commands. COMPUTE. modeller. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="be240-126">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="be240-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be240-127">NOTES</span></span>

## <span data-ttu-id="be240-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be240-128">RELATED LINKS</span></span>

[<span data-ttu-id="be240-129">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="be240-129">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)


