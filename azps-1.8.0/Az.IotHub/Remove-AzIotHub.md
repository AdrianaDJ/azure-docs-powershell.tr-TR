---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 1529b7b70ec25a7ee8f4b047e28fe77efaf92351
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916432"
---
# <span data-ttu-id="8f8a6-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="8f8a6-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="8f8a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f8a6-102">SYNOPSIS</span></span>
<span data-ttu-id="8f8a6-103">Bir IotHub siler.</span><span class="sxs-lookup"><span data-stu-id="8f8a6-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="8f8a6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8f8a6-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f8a6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8f8a6-105">DESCRIPTION</span></span>
<span data-ttu-id="8f8a6-106">Bir IotHub siler.</span><span class="sxs-lookup"><span data-stu-id="8f8a6-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="8f8a6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8f8a6-107">EXAMPLES</span></span>

### <span data-ttu-id="8f8a6-108">Örnek 1 IotHub</span><span class="sxs-lookup"><span data-stu-id="8f8a6-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="8f8a6-109">"Myiothub" adındaki bir IotHub kaldırır</span><span class="sxs-lookup"><span data-stu-id="8f8a6-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="8f8a6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8f8a6-110">PARAMETERS</span></span>

### <span data-ttu-id="8f8a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f8a6-111">-DefaultProfile</span></span>
<span data-ttu-id="8f8a6-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8f8a6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f8a6-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="8f8a6-113">-Name</span></span>
<span data-ttu-id="8f8a6-114">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="8f8a6-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="8f8a6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f8a6-115">-ResourceGroupName</span></span>
<span data-ttu-id="8f8a6-116">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="8f8a6-116">Resource Group Name</span></span>

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

### <span data-ttu-id="8f8a6-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="8f8a6-117">-Confirm</span></span>
<span data-ttu-id="8f8a6-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8f8a6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f8a6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f8a6-119">-WhatIf</span></span>
<span data-ttu-id="8f8a6-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8f8a6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f8a6-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8f8a6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f8a6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f8a6-122">CommonParameters</span></span>
<span data-ttu-id="8f8a6-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8f8a6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f8a6-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f8a6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f8a6-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8f8a6-125">INPUTS</span></span>

### <span data-ttu-id="8f8a6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8f8a6-126">System.String</span></span>

## <span data-ttu-id="8f8a6-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8f8a6-127">OUTPUTS</span></span>

### <span data-ttu-id="8f8a6-128">System. void</span><span class="sxs-lookup"><span data-stu-id="8f8a6-128">System.Void</span></span>

## <span data-ttu-id="8f8a6-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8f8a6-129">NOTES</span></span>

## <span data-ttu-id="8f8a6-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8f8a6-130">RELATED LINKS</span></span>
