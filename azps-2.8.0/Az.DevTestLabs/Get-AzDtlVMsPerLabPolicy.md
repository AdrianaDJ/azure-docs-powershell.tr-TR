---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 2603a9c5f259de05b466693bdc42d7a6dfb2eda2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752088"
---
# <span data-ttu-id="10ecf-101">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="10ecf-101">Get-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="10ecf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="10ecf-103">DevTest laboratuvarlarında bir laboratuvarın laboratuar politikası başına sanal makine alır.</span><span class="sxs-lookup"><span data-stu-id="10ecf-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="10ecf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="10ecf-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10ecf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="10ecf-105">DESCRIPTION</span></span>
<span data-ttu-id="10ecf-106">**Get-AzDtlVMsPerLabPolicy** cmdlet 'i bir laboratuvarın laboratuvar politikası başına sanal makineleri alır ve bir laboratuvarda izin verilen toplam sanal makine sayısını ayarlamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="10ecf-106">The **Get-AzDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="10ecf-107">Cmdlet ilkenin etkin veya devre dışı durumunu ve ilkede ayarlamış olduğunuz laboratuvarda izin verilen toplam sanal makine sayısını döndürür.</span><span class="sxs-lookup"><span data-stu-id="10ecf-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="10ecf-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="10ecf-108">EXAMPLES</span></span>

## <span data-ttu-id="10ecf-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="10ecf-109">PARAMETERS</span></span>

### <span data-ttu-id="10ecf-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10ecf-110">-DefaultProfile</span></span>
<span data-ttu-id="10ecf-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="10ecf-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10ecf-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="10ecf-112">-LabName</span></span>
<span data-ttu-id="10ecf-113">Bu cmdlet 'in sanal makineleri aldığı laboratuarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10ecf-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="10ecf-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10ecf-114">-ResourceGroupName</span></span>
<span data-ttu-id="10ecf-115">Laboratuarın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10ecf-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="10ecf-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10ecf-116">CommonParameters</span></span>
<span data-ttu-id="10ecf-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="10ecf-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10ecf-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10ecf-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10ecf-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="10ecf-119">INPUTS</span></span>

### <span data-ttu-id="10ecf-120">System. String</span><span class="sxs-lookup"><span data-stu-id="10ecf-120">System.String</span></span>

## <span data-ttu-id="10ecf-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="10ecf-121">OUTPUTS</span></span>

### <span data-ttu-id="10ecf-122">Microsoft. Azure. Commands. DevTestLabs. model. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="10ecf-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="10ecf-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="10ecf-123">NOTES</span></span>

## <span data-ttu-id="10ecf-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="10ecf-124">RELATED LINKS</span></span>

[<span data-ttu-id="10ecf-125">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="10ecf-125">Set-AzDtlVMsPerLabPolicy</span></span>](./Set-AzDtlVMsPerLabPolicy.md)


