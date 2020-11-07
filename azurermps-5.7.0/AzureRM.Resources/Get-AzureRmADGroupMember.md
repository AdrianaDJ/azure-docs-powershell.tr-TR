---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
ms.openlocfilehash: c3a783178bf8342e891f8eab2996e77a2045721a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763554"
---
# <span data-ttu-id="e13cd-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="e13cd-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="e13cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e13cd-102">SYNOPSIS</span></span>
<span data-ttu-id="e13cd-103">Grup üyelerini edinin.</span><span class="sxs-lookup"><span data-stu-id="e13cd-103">Get a group members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e13cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e13cd-104">SYNTAX</span></span>

```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e13cd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e13cd-105">DESCRIPTION</span></span>
<span data-ttu-id="e13cd-106">Grup üyelerini edinin.</span><span class="sxs-lookup"><span data-stu-id="e13cd-106">Get a group members.</span></span>

## <span data-ttu-id="e13cd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e13cd-107">EXAMPLES</span></span>

### <span data-ttu-id="e13cd-108">Grup nesnesi kimliği kullanan grup üyelerine filtre uygular</span><span class="sxs-lookup"><span data-stu-id="e13cd-108">Filters group members using group object id</span></span>
```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="e13cd-109">85 F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ID ile grup üyelerini alır</span><span class="sxs-lookup"><span data-stu-id="e13cd-109">Gets group members with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

## <span data-ttu-id="e13cd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e13cd-110">PARAMETERS</span></span>

### <span data-ttu-id="e13cd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e13cd-111">-DefaultProfile</span></span>
<span data-ttu-id="e13cd-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e13cd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e13cd-113">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="e13cd-113">-GroupObjectId</span></span>
<span data-ttu-id="e13cd-114">Grubun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="e13cd-114">Object id of the group.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e13cd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e13cd-115">CommonParameters</span></span>
<span data-ttu-id="e13cd-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e13cd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e13cd-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e13cd-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e13cd-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e13cd-118">INPUTS</span></span>

### <span data-ttu-id="e13cd-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e13cd-119">None</span></span>
<span data-ttu-id="e13cd-120">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e13cd-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e13cd-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e13cd-121">OUTPUTS</span></span>

### <span data-ttu-id="e13cd-122">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADObject]</span><span class="sxs-lookup"><span data-stu-id="e13cd-122">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject]</span></span>

## <span data-ttu-id="e13cd-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e13cd-123">NOTES</span></span>

## <span data-ttu-id="e13cd-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e13cd-124">RELATED LINKS</span></span>

[<span data-ttu-id="e13cd-125">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="e13cd-125">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="e13cd-126">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e13cd-126">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

