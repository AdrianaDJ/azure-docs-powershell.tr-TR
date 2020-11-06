---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
ms.openlocfilehash: 17d7f922f5af46aa99e3b01aa0c0f63df05effe7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589123"
---
# <span data-ttu-id="b75fb-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="b75fb-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="b75fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b75fb-102">SYNOPSIS</span></span>
<span data-ttu-id="b75fb-103">Grup üyelerini edinin.</span><span class="sxs-lookup"><span data-stu-id="b75fb-103">Get a group members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b75fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b75fb-104">SYNTAX</span></span>

```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b75fb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b75fb-105">DESCRIPTION</span></span>
<span data-ttu-id="b75fb-106">Grup üyelerini edinin.</span><span class="sxs-lookup"><span data-stu-id="b75fb-106">Get a group members.</span></span>

## <span data-ttu-id="b75fb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b75fb-107">EXAMPLES</span></span>

### <span data-ttu-id="b75fb-108">--------------------------Grup--------------------------nesnesi</span><span class="sxs-lookup"><span data-stu-id="b75fb-108">--------------------------  Filters group members using group object id  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="b75fb-109">85 F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ID ile grup üyelerini alır</span><span class="sxs-lookup"><span data-stu-id="b75fb-109">Gets group members with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

## <span data-ttu-id="b75fb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b75fb-110">PARAMETERS</span></span>

### <span data-ttu-id="b75fb-111">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="b75fb-111">-GroupObjectId</span></span>
<span data-ttu-id="b75fb-112">Grubun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="b75fb-112">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b75fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b75fb-113">-DefaultProfile</span></span>
<span data-ttu-id="b75fb-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b75fb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b75fb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b75fb-115">CommonParameters</span></span>
<span data-ttu-id="b75fb-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b75fb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b75fb-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b75fb-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b75fb-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b75fb-118">INPUTS</span></span>

## <span data-ttu-id="b75fb-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b75fb-119">OUTPUTS</span></span>

### <span data-ttu-id="b75fb-120">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADObject]</span><span class="sxs-lookup"><span data-stu-id="b75fb-120">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject]</span></span>

## <span data-ttu-id="b75fb-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b75fb-121">NOTES</span></span>

## <span data-ttu-id="b75fb-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b75fb-122">RELATED LINKS</span></span>

[<span data-ttu-id="b75fb-123">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="b75fb-123">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="b75fb-124">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b75fb-124">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

