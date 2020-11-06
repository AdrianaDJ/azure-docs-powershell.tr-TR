---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
ms.openlocfilehash: 8c2f6a45bb483109b61be47de3013f3ccb4d5c19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592735"
---
# <span data-ttu-id="784b6-101">Remove-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="784b6-101">Remove-AzureRmSecurityContact</span></span>

## <span data-ttu-id="784b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="784b6-102">SYNOPSIS</span></span>
<span data-ttu-id="784b6-103">Güvenlik kişisini siler.</span><span class="sxs-lookup"><span data-stu-id="784b6-103">Deletes a security contact.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="784b6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="784b6-104">SYNTAX</span></span>

### <span data-ttu-id="784b6-105">SubscriptionLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="784b6-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzureRmSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="784b6-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="784b6-106">ResourceId</span></span>
```
Remove-AzureRmSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="784b6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="784b6-107">InputObject</span></span>
```
Remove-AzureRmSecurityContact -InputObject <PSRemoveSecurityContactInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="784b6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="784b6-108">DESCRIPTION</span></span>
<span data-ttu-id="784b6-109">Güvenlik kişisini siler.</span><span class="sxs-lookup"><span data-stu-id="784b6-109">Deletes a security contact.</span></span>

## <span data-ttu-id="784b6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="784b6-110">EXAMPLES</span></span>

### <span data-ttu-id="784b6-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="784b6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSecurityContact -Name "default1"
```

<span data-ttu-id="784b6-112">"Default1" güvenlik kişisini siler</span><span class="sxs-lookup"><span data-stu-id="784b6-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="784b6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="784b6-113">PARAMETERS</span></span>

### <span data-ttu-id="784b6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="784b6-114">-DefaultProfile</span></span>
<span data-ttu-id="784b6-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="784b6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="784b6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="784b6-116">-InputObject</span></span>
<span data-ttu-id="784b6-117">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="784b6-117">Input Object.</span></span>

```yaml
Type: PSRemoveSecurityContactInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="784b6-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="784b6-118">-Name</span></span>
<span data-ttu-id="784b6-119">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="784b6-119">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="784b6-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="784b6-120">-PassThru</span></span>
<span data-ttu-id="784b6-121">İşlemin başarılı olup olmadığını döndürün.</span><span class="sxs-lookup"><span data-stu-id="784b6-121">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="784b6-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="784b6-122">-ResourceId</span></span>
<span data-ttu-id="784b6-123">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="784b6-123">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="784b6-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="784b6-124">-Confirm</span></span>
<span data-ttu-id="784b6-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="784b6-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="784b6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="784b6-126">-WhatIf</span></span>
<span data-ttu-id="784b6-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="784b6-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="784b6-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="784b6-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="784b6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="784b6-129">CommonParameters</span></span>
<span data-ttu-id="784b6-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="784b6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="784b6-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="784b6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="784b6-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="784b6-132">INPUTS</span></span>

### <span data-ttu-id="784b6-133">System. String</span><span class="sxs-lookup"><span data-stu-id="784b6-133">System.String</span></span>
<span data-ttu-id="784b6-134">Microsoft. Azure. Commands. Security. cmdlet. Securitcontacts. PSRemoveSecurityContactInputObject</span><span class="sxs-lookup"><span data-stu-id="784b6-134">Microsoft.Azure.Commands.Security.Cmdlets.SecurityContacts.PSRemoveSecurityContactInputObject</span></span>

## <span data-ttu-id="784b6-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="784b6-135">OUTPUTS</span></span>

### <span data-ttu-id="784b6-136">Microsoft. Azure. Commands. Security. model. Securitcontacts. Pssecuritycontacts</span><span class="sxs-lookup"><span data-stu-id="784b6-136">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="784b6-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="784b6-137">NOTES</span></span>

## <span data-ttu-id="784b6-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="784b6-138">RELATED LINKS</span></span>
