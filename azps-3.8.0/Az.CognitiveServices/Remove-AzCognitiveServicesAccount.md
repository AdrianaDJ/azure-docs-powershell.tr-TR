---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
ms.openlocfilehash: 1069365bb04cdf9a6d873e6fa86c61619b6d0dab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095779"
---
# <span data-ttu-id="01155-101">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="01155-101">Remove-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="01155-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01155-102">SYNOPSIS</span></span>
<span data-ttu-id="01155-103">Bir öğretici hizmetler hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="01155-103">Deletes a Cognitive Services account.</span></span>

## <span data-ttu-id="01155-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01155-104">SYNTAX</span></span>

```
Remove-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01155-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="01155-105">DESCRIPTION</span></span>
<span data-ttu-id="01155-106">**Remove-Azsitiveservicesaccount** cmdlet 'i, belirtilen öğretici sitif hizmetler hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="01155-106">The **Remove-AzCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="01155-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01155-107">EXAMPLES</span></span>

### <span data-ttu-id="01155-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="01155-108">Example 1</span></span>
<span data-ttu-id="01155-109">Bu komut hiçbir şey döndürmez.</span><span class="sxs-lookup"><span data-stu-id="01155-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="01155-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01155-110">PARAMETERS</span></span>

### <span data-ttu-id="01155-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01155-111">-DefaultProfile</span></span>
<span data-ttu-id="01155-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="01155-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01155-113">-Force</span><span class="sxs-lookup"><span data-stu-id="01155-113">-Force</span></span>
<span data-ttu-id="01155-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="01155-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01155-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="01155-115">-Name</span></span>
<span data-ttu-id="01155-116">Silinecek hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01155-116">Specifies the name of the account to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01155-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01155-117">-ResourceGroupName</span></span>
<span data-ttu-id="01155-118">Öğretici hizmetler hesabının atandığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01155-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="01155-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="01155-119">-Confirm</span></span>
<span data-ttu-id="01155-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="01155-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01155-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01155-121">-WhatIf</span></span>
<span data-ttu-id="01155-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="01155-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01155-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="01155-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01155-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01155-124">CommonParameters</span></span>
<span data-ttu-id="01155-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01155-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01155-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="01155-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01155-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01155-127">INPUTS</span></span>

### <span data-ttu-id="01155-128">System. String</span><span class="sxs-lookup"><span data-stu-id="01155-128">System.String</span></span>

## <span data-ttu-id="01155-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01155-129">OUTPUTS</span></span>

### <span data-ttu-id="01155-130">System. void</span><span class="sxs-lookup"><span data-stu-id="01155-130">System.Void</span></span>

## <span data-ttu-id="01155-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01155-131">NOTES</span></span>

## <span data-ttu-id="01155-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01155-132">RELATED LINKS</span></span>

[<span data-ttu-id="01155-133">Get-Azsitiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="01155-133">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="01155-134">Yeni-Azsitiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="01155-134">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="01155-135">Set-Azsiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="01155-135">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)

