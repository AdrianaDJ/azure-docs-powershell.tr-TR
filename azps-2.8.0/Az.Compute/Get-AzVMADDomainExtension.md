---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: 2ec4ec1898e79fd7f7f35a406f2a99f9dd2da6fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752935"
---
# <span data-ttu-id="43471-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="43471-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="43471-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43471-102">SYNOPSIS</span></span>
<span data-ttu-id="43471-103">AD etki alanı uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="43471-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="43471-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="43471-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43471-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="43471-105">DESCRIPTION</span></span>
<span data-ttu-id="43471-106">**Get-AzVMADDomainExtension** cmdlet 'ı belirtilen Azure Active DIRECTORY (ad) etki alanı uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="43471-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="43471-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="43471-107">EXAMPLES</span></span>

## <span data-ttu-id="43471-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="43471-108">PARAMETERS</span></span>

### <span data-ttu-id="43471-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43471-109">-DefaultProfile</span></span>
<span data-ttu-id="43471-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="43471-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43471-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="43471-111">-Name</span></span>
<span data-ttu-id="43471-112">Etki alanı uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43471-112">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="43471-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43471-113">-ResourceGroupName</span></span>
<span data-ttu-id="43471-114">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43471-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="43471-115">-Durum</span><span class="sxs-lookup"><span data-stu-id="43471-115">-Status</span></span>
<span data-ttu-id="43471-116">Bu cmdlet 'in etki alanı uzantısının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="43471-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="43471-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="43471-117">-VMName</span></span>
<span data-ttu-id="43471-118">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43471-118">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="43471-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43471-119">CommonParameters</span></span>
<span data-ttu-id="43471-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="43471-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43471-121">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="43471-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43471-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="43471-122">INPUTS</span></span>

### <span data-ttu-id="43471-123">System. String</span><span class="sxs-lookup"><span data-stu-id="43471-123">System.String</span></span>

### <span data-ttu-id="43471-124">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="43471-124">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="43471-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="43471-125">OUTPUTS</span></span>

### <span data-ttu-id="43471-126">Microsoft. Azure. Commands. COMPUTE. modeller. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="43471-126">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="43471-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="43471-127">NOTES</span></span>

## <span data-ttu-id="43471-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="43471-128">RELATED LINKS</span></span>

[<span data-ttu-id="43471-129">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="43471-129">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)


