---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: 2be26f222be7ec444706fb15fb862a43dc8b8116
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593144"
---
# <span data-ttu-id="91b26-101">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="91b26-101">Get-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="91b26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91b26-102">SYNOPSIS</span></span>
<span data-ttu-id="91b26-103">DevTest laboratuvarlarında bir laboratuarın Kullanıcı başına sanal makine ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="91b26-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91b26-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91b26-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91b26-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="91b26-105">DESCRIPTION</span></span>
<span data-ttu-id="91b26-106">**Get-AzureRmDtlVMsPerUserPolicy** cmdlet 'i, bir laboratuvarın Kullanıcı başına sanal makinelerini alır ve Kullanıcı başına izin verilen en fazla sanal makine sayısını ayarlamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="91b26-106">The **Get-AzureRmDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="91b26-107">Cmdlet, ilkenin etkin veya devre dışı durumunu ve ilkede ayarladığınız Kullanıcı başına izin verilen en fazla sanal makine sayısını döndürür.</span><span class="sxs-lookup"><span data-stu-id="91b26-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="91b26-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91b26-108">EXAMPLES</span></span>

## <span data-ttu-id="91b26-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91b26-109">PARAMETERS</span></span>

### <span data-ttu-id="91b26-110">-LabName</span><span class="sxs-lookup"><span data-stu-id="91b26-110">-LabName</span></span>
<span data-ttu-id="91b26-111">Bu cmdlet 'in Kullanıcı başına sanal makineyi aldığı laboratuarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91b26-111">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="91b26-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91b26-112">-ResourceGroupName</span></span>
<span data-ttu-id="91b26-113">Laboratuarın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91b26-113">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="91b26-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91b26-114">-DefaultProfile</span></span>
<span data-ttu-id="91b26-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="91b26-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91b26-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91b26-116">CommonParameters</span></span>
<span data-ttu-id="91b26-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91b26-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91b26-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91b26-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91b26-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91b26-119">INPUTS</span></span>

## <span data-ttu-id="91b26-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91b26-120">OUTPUTS</span></span>

### <span data-ttu-id="91b26-121">Microsoft. Azure. Commands. DevTestLabs. model. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="91b26-121">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="91b26-122">Bu cmdlet, laboratuarda bir kullanıcı tarafından oluşturulabilen en fazla sanal makine sayısını belirten ilkeyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="91b26-122">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="91b26-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91b26-123">NOTES</span></span>

## <span data-ttu-id="91b26-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91b26-124">RELATED LINKS</span></span>

[<span data-ttu-id="91b26-125">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="91b26-125">Set-AzureRmDtlVMsPerUserPolicy</span></span>](./Set-AzureRmDtlVMsPerUserPolicy.md)

