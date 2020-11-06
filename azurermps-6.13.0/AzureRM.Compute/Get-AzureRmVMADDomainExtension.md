---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
ms.openlocfilehash: 398cc4b8f23ca5296aec741eb720833f589b0e2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588554"
---
# <span data-ttu-id="00b50-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="00b50-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="00b50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00b50-102">SYNOPSIS</span></span>
<span data-ttu-id="00b50-103">AD etki alanı uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="00b50-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00b50-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00b50-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00b50-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="00b50-105">DESCRIPTION</span></span>
<span data-ttu-id="00b50-106">**Get-AzureRmVMADDomainExtension** cmdlet 'ı belirtilen Azure Active DIRECTORY (ad) etki alanı uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="00b50-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="00b50-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00b50-107">EXAMPLES</span></span>

## <span data-ttu-id="00b50-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00b50-108">PARAMETERS</span></span>

### <span data-ttu-id="00b50-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00b50-109">-DefaultProfile</span></span>
<span data-ttu-id="00b50-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="00b50-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00b50-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="00b50-111">-Name</span></span>
<span data-ttu-id="00b50-112">Etki alanı uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00b50-112">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="00b50-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00b50-113">-ResourceGroupName</span></span>
<span data-ttu-id="00b50-114">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00b50-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="00b50-115">-Durum</span><span class="sxs-lookup"><span data-stu-id="00b50-115">-Status</span></span>
<span data-ttu-id="00b50-116">Bu cmdlet 'in etki alanı uzantısının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="00b50-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="00b50-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="00b50-117">-VMName</span></span>
<span data-ttu-id="00b50-118">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00b50-118">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="00b50-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00b50-119">CommonParameters</span></span>
<span data-ttu-id="00b50-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00b50-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00b50-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00b50-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00b50-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00b50-122">INPUTS</span></span>

### <span data-ttu-id="00b50-123">System. String</span><span class="sxs-lookup"><span data-stu-id="00b50-123">System.String</span></span>

### <span data-ttu-id="00b50-124">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="00b50-124">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="00b50-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00b50-125">OUTPUTS</span></span>

### <span data-ttu-id="00b50-126">Microsoft. Azure. Commands. COMPUTE. modeller. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="00b50-126">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="00b50-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00b50-127">NOTES</span></span>

## <span data-ttu-id="00b50-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00b50-128">RELATED LINKS</span></span>

[<span data-ttu-id="00b50-129">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="00b50-129">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


