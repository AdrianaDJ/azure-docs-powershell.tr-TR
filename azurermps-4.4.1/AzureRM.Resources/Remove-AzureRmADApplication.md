---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
ms.openlocfilehash: 0b0b560a97e223820a3a73ce036a5d7599df9a46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592559"
---
# <span data-ttu-id="85b4d-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="85b4d-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="85b4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85b4d-102">SYNOPSIS</span></span>
<span data-ttu-id="85b4d-103">Azure Active Directory uygulamasını siler.</span><span class="sxs-lookup"><span data-stu-id="85b4d-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85b4d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="85b4d-104">SYNTAX</span></span>

```
Remove-AzureRmADApplication -ObjectId <Guid> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85b4d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="85b4d-105">DESCRIPTION</span></span>
<span data-ttu-id="85b4d-106">Azure Active Directory uygulamasını siler.</span><span class="sxs-lookup"><span data-stu-id="85b4d-106">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="85b4d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="85b4d-107">EXAMPLES</span></span>

### <span data-ttu-id="85b4d-108">AAD uygulamasını silme--------------------------.</span><span class="sxs-lookup"><span data-stu-id="85b4d-108">--------------------------  Delete AAD application.</span></span>  --------------------------
```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 -Force
```

<span data-ttu-id="85b4d-109">Azure Active Directory uygulamasını siler.</span><span class="sxs-lookup"><span data-stu-id="85b4d-109">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="85b4d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="85b4d-110">PARAMETERS</span></span>

### <span data-ttu-id="85b4d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="85b4d-111">-Force</span></span>
<span data-ttu-id="85b4d-112">Onaysız uygulamayı silme düğmesi.</span><span class="sxs-lookup"><span data-stu-id="85b4d-112">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="85b4d-113">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="85b4d-113">-ObjectId</span></span>
<span data-ttu-id="85b4d-114">Silinecek uygulamanın nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="85b4d-114">The object id of the application to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85b4d-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="85b4d-115">-Confirm</span></span>
<span data-ttu-id="85b4d-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="85b4d-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85b4d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85b4d-117">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85b4d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85b4d-118">-DefaultProfile</span></span>
<span data-ttu-id="85b4d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="85b4d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85b4d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85b4d-120">CommonParameters</span></span>
<span data-ttu-id="85b4d-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="85b4d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85b4d-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85b4d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85b4d-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="85b4d-123">INPUTS</span></span>

## <span data-ttu-id="85b4d-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="85b4d-124">OUTPUTS</span></span>

## <span data-ttu-id="85b4d-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="85b4d-125">NOTES</span></span>
<span data-ttu-id="85b4d-126">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="85b4d-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="85b4d-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="85b4d-127">RELATED LINKS</span></span>

[<span data-ttu-id="85b4d-128">Yeni-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="85b4d-128">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="85b4d-129">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="85b4d-129">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="85b4d-130">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="85b4d-130">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="85b4d-131">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="85b4d-131">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
