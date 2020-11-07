---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 0a2350cf3e1c8619e1860a6a5c4a0832c978d9de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763626"
---
# <span data-ttu-id="f01c4-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f01c4-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="f01c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f01c4-102">SYNOPSIS</span></span>
<span data-ttu-id="f01c4-103">Azure Active Directory hizmet sorumlusunu siler.</span><span class="sxs-lookup"><span data-stu-id="f01c4-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f01c4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f01c4-104">SYNTAX</span></span>

```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f01c4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f01c4-105">DESCRIPTION</span></span>
<span data-ttu-id="f01c4-106">Azure Active Directory hizmet sorumlusunu siler.</span><span class="sxs-lookup"><span data-stu-id="f01c4-106">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="f01c4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f01c4-107">EXAMPLES</span></span>

### <span data-ttu-id="f01c4-108">AAD hizmet sorumlusunu silme--------------------------.</span><span class="sxs-lookup"><span data-stu-id="f01c4-108">--------------------------  Delete AAD service principal.</span></span>  --------------------------
```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="f01c4-109">Verilen Azure Active Directory hizmet sorumlusunu siler.</span><span class="sxs-lookup"><span data-stu-id="f01c4-109">Deletes the given azure active directory service principal.</span></span>

## <span data-ttu-id="f01c4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f01c4-110">PARAMETERS</span></span>

### <span data-ttu-id="f01c4-111">-Force</span><span class="sxs-lookup"><span data-stu-id="f01c4-111">-Force</span></span>
<span data-ttu-id="f01c4-112">{{Fill Force açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="f01c4-112">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="f01c4-113">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="f01c4-113">-ObjectId</span></span>
<span data-ttu-id="f01c4-114">Silinecek hizmet sorumlusunun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="f01c4-114">The object id of the service principal to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f01c4-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f01c4-115">-PassThru</span></span>
<span data-ttu-id="f01c4-116">Belirtilmişse, silinmiş hizmet sorumlusunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="f01c4-116">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="f01c4-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="f01c4-117">-Confirm</span></span>
<span data-ttu-id="f01c4-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f01c4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f01c4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f01c4-119">-WhatIf</span></span>
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

### <span data-ttu-id="f01c4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f01c4-120">-DefaultProfile</span></span>
<span data-ttu-id="f01c4-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f01c4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f01c4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f01c4-122">CommonParameters</span></span>
<span data-ttu-id="f01c4-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f01c4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f01c4-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f01c4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f01c4-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f01c4-125">INPUTS</span></span>

## <span data-ttu-id="f01c4-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f01c4-126">OUTPUTS</span></span>

### <span data-ttu-id="f01c4-127">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f01c4-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="f01c4-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f01c4-128">NOTES</span></span>
<span data-ttu-id="f01c4-129">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="f01c4-129">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="f01c4-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f01c4-130">RELATED LINKS</span></span>

[<span data-ttu-id="f01c4-131">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f01c4-131">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="f01c4-132">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f01c4-132">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="f01c4-133">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f01c4-133">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="f01c4-134">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="f01c4-134">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="f01c4-135">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f01c4-135">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
