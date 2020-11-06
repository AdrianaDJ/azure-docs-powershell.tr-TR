---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerLabPolicy.md
ms.openlocfilehash: 3f38c8ace41a1f125a37053f136cd61c597787ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589558"
---
# <span data-ttu-id="a1cd2-101">Get-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="a1cd2-101">Get-AzureRmDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="a1cd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1cd2-102">SYNOPSIS</span></span>
<span data-ttu-id="a1cd2-103">DevTest laboratuvarlarında bir laboratuvarın laboratuar politikası başına sanal makine alır.</span><span class="sxs-lookup"><span data-stu-id="a1cd2-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1cd2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1cd2-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1cd2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1cd2-105">DESCRIPTION</span></span>
<span data-ttu-id="a1cd2-106">**Get-AzureRmDtlVMsPerLabPolicy** cmdlet 'i bir laboratuvarın laboratuvar politikası başına sanal makineleri alır ve bir laboratuvarda izin verilen toplam sanal makine sayısını ayarlamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="a1cd2-106">The **Get-AzureRmDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="a1cd2-107">Cmdlet ilkenin etkin veya devre dışı durumunu ve ilkede ayarlamış olduğunuz laboratuvarda izin verilen toplam sanal makine sayısını döndürür.</span><span class="sxs-lookup"><span data-stu-id="a1cd2-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="a1cd2-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1cd2-108">EXAMPLES</span></span>

## <span data-ttu-id="a1cd2-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1cd2-109">PARAMETERS</span></span>

### <span data-ttu-id="a1cd2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1cd2-110">-DefaultProfile</span></span>
<span data-ttu-id="a1cd2-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a1cd2-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1cd2-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="a1cd2-112">-LabName</span></span>
<span data-ttu-id="a1cd2-113">Bu cmdlet 'in sanal makineleri aldığı laboratuarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1cd2-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="a1cd2-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1cd2-114">-ResourceGroupName</span></span>
<span data-ttu-id="a1cd2-115">Laboratuarın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1cd2-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cd2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1cd2-116">CommonParameters</span></span>
<span data-ttu-id="a1cd2-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1cd2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1cd2-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1cd2-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1cd2-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1cd2-119">INPUTS</span></span>

### <span data-ttu-id="a1cd2-120">System. String</span><span class="sxs-lookup"><span data-stu-id="a1cd2-120">System.String</span></span>

## <span data-ttu-id="a1cd2-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1cd2-121">OUTPUTS</span></span>

### <span data-ttu-id="a1cd2-122">Microsoft. Azure. Commands. DevTestLabs. model. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="a1cd2-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="a1cd2-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1cd2-123">NOTES</span></span>

## <span data-ttu-id="a1cd2-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1cd2-124">RELATED LINKS</span></span>

[<span data-ttu-id="a1cd2-125">Set-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="a1cd2-125">Set-AzureRmDtlVMsPerLabPolicy</span></span>](./Set-AzureRmDtlVMsPerLabPolicy.md)


