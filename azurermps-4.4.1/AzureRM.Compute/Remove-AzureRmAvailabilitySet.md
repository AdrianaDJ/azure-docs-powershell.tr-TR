---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
ms.openlocfilehash: 796000ac20ab887d4abd26039da2a111a19141ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591113"
---
# <span data-ttu-id="8b9ac-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8b9ac-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="8b9ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b9ac-102">SYNOPSIS</span></span>
<span data-ttu-id="8b9ac-103">Azure 'dan bir kullanılabilirlik kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b9ac-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b9ac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b9ac-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b9ac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b9ac-105">DESCRIPTION</span></span>
<span data-ttu-id="8b9ac-106">**Remove-AzureRmAvailabilitySet** cmdlet 'i Azure 'dan bir kullanılabilirlik kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b9ac-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="8b9ac-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b9ac-107">EXAMPLES</span></span>

### <span data-ttu-id="8b9ac-108">Örnek 1: kullanılabilirlik kümesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="8b9ac-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="8b9ac-109">Bu komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki bir kullanılabilirlik kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b9ac-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="8b9ac-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b9ac-110">PARAMETERS</span></span>

### <span data-ttu-id="8b9ac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b9ac-111">-DefaultProfile</span></span>
<span data-ttu-id="8b9ac-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8b9ac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b9ac-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8b9ac-113">-Force</span></span>
<span data-ttu-id="8b9ac-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="8b9ac-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b9ac-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="8b9ac-115">-Name</span></span>
<span data-ttu-id="8b9ac-116">Kullanılabilirlik kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="8b9ac-116">The availability set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b9ac-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b9ac-117">-ResourceGroupName</span></span>
<span data-ttu-id="8b9ac-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b9ac-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8b9ac-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="8b9ac-119">-Confirm</span></span>
<span data-ttu-id="8b9ac-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8b9ac-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b9ac-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b9ac-121">-WhatIf</span></span>
<span data-ttu-id="8b9ac-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b9ac-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="8b9ac-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8b9ac-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b9ac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b9ac-124">CommonParameters</span></span>
<span data-ttu-id="8b9ac-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b9ac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b9ac-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b9ac-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b9ac-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b9ac-127">INPUTS</span></span>

## <span data-ttu-id="8b9ac-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b9ac-128">OUTPUTS</span></span>

## <span data-ttu-id="8b9ac-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b9ac-129">NOTES</span></span>

## <span data-ttu-id="8b9ac-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b9ac-130">RELATED LINKS</span></span>

[<span data-ttu-id="8b9ac-131">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8b9ac-131">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="8b9ac-132">Yeni-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8b9ac-132">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

