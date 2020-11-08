---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: b4cbecd2e29a0b70c7e62194df2364b22b33b462
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276731"
---
# <span data-ttu-id="72065-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="72065-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="72065-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72065-102">SYNOPSIS</span></span>
<span data-ttu-id="72065-103">Güvenlik kişisini siler.</span><span class="sxs-lookup"><span data-stu-id="72065-103">Deletes a security contact.</span></span>

## <span data-ttu-id="72065-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72065-104">SYNTAX</span></span>

### <span data-ttu-id="72065-105">SubscriptionLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="72065-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72065-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="72065-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72065-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="72065-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72065-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="72065-108">DESCRIPTION</span></span>
<span data-ttu-id="72065-109">Güvenlik kişisini siler.</span><span class="sxs-lookup"><span data-stu-id="72065-109">Deletes a security contact.</span></span>

## <span data-ttu-id="72065-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72065-110">EXAMPLES</span></span>

### <span data-ttu-id="72065-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="72065-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="72065-112">"Default1" güvenlik kişisini siler</span><span class="sxs-lookup"><span data-stu-id="72065-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="72065-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72065-113">PARAMETERS</span></span>

### <span data-ttu-id="72065-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72065-114">-DefaultProfile</span></span>
<span data-ttu-id="72065-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="72065-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72065-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72065-116">-InputObject</span></span>
<span data-ttu-id="72065-117">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="72065-117">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72065-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="72065-118">-Name</span></span>
<span data-ttu-id="72065-119">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="72065-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72065-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="72065-120">-PassThru</span></span>
<span data-ttu-id="72065-121">İşlemin başarılı olup olmadığını döndürün.</span><span class="sxs-lookup"><span data-stu-id="72065-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="72065-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="72065-122">-ResourceId</span></span>
<span data-ttu-id="72065-123">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="72065-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72065-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="72065-124">-Confirm</span></span>
<span data-ttu-id="72065-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="72065-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72065-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72065-126">-WhatIf</span></span>
<span data-ttu-id="72065-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72065-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72065-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="72065-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72065-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72065-129">CommonParameters</span></span>
<span data-ttu-id="72065-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72065-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72065-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="72065-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72065-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72065-132">INPUTS</span></span>

### <span data-ttu-id="72065-133">System. String</span><span class="sxs-lookup"><span data-stu-id="72065-133">System.String</span></span>

### <span data-ttu-id="72065-134">Microsoft. Azure. Commands. Security. model. Securitcontacts. Pssecuritycontacts</span><span class="sxs-lookup"><span data-stu-id="72065-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="72065-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72065-135">OUTPUTS</span></span>

### <span data-ttu-id="72065-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72065-136">System.Boolean</span></span>

## <span data-ttu-id="72065-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72065-137">NOTES</span></span>

## <span data-ttu-id="72065-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72065-138">RELATED LINKS</span></span>
