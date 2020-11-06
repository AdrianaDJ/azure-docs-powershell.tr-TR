---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: a182bed0e93492521e3ac46d5f0ed3e2d705394c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594814"
---
# <span data-ttu-id="b0732-101">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b0732-101">Remove-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="b0732-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0732-102">SYNOPSIS</span></span>
<span data-ttu-id="b0732-103">Bir öğretici hizmetler hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="b0732-103">Deletes a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0732-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b0732-104">SYNTAX</span></span>

```
Remove-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0732-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b0732-105">DESCRIPTION</span></span>
<span data-ttu-id="b0732-106">**Remove-Azurermöğretici Iveservicesaccount** cmdlet 'ı belirtilen öğretici sitif hizmetler hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="b0732-106">The **Remove-AzureRmCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="b0732-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b0732-107">EXAMPLES</span></span>

## <span data-ttu-id="b0732-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b0732-108">PARAMETERS</span></span>

### <span data-ttu-id="b0732-109">-Force</span><span class="sxs-lookup"><span data-stu-id="b0732-109">-Force</span></span>
<span data-ttu-id="b0732-110">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b0732-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b0732-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="b0732-111">-Name</span></span>
<span data-ttu-id="b0732-112">Silinecek hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0732-112">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="b0732-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0732-113">-ResourceGroupName</span></span>
<span data-ttu-id="b0732-114">Öğretici hizmetler hesabının atandığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0732-114">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="b0732-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="b0732-115">-Confirm</span></span>
<span data-ttu-id="b0732-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b0732-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0732-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0732-117">-WhatIf</span></span>
<span data-ttu-id="b0732-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b0732-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0732-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b0732-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0732-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0732-120">-DefaultProfile</span></span>
<span data-ttu-id="b0732-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b0732-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0732-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0732-122">CommonParameters</span></span>
<span data-ttu-id="b0732-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b0732-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0732-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0732-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0732-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b0732-125">INPUTS</span></span>

## <span data-ttu-id="b0732-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b0732-126">OUTPUTS</span></span>

## <span data-ttu-id="b0732-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b0732-127">NOTES</span></span>

## <span data-ttu-id="b0732-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b0732-128">RELATED LINKS</span></span>

[<span data-ttu-id="b0732-129">Get-Azurermöğretici Itiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="b0732-129">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="b0732-130">Yeni-Azurermöğretici</span><span class="sxs-lookup"><span data-stu-id="b0732-130">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="b0732-131">Set-Azurermöğretici Itiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="b0732-131">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


