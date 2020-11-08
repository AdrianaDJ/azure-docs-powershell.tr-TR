---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 79780c101296d78115a1c88ef4d4aebcd3721c22
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097061"
---
# <span data-ttu-id="23ce2-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="23ce2-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="23ce2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23ce2-102">SYNOPSIS</span></span>
<span data-ttu-id="23ce2-103">Bu aboneliğin güvenlik çalışma alanı ayarını siler.</span><span class="sxs-lookup"><span data-stu-id="23ce2-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="23ce2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23ce2-104">SYNTAX</span></span>

### <span data-ttu-id="23ce2-105">SubscriptionLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="23ce2-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23ce2-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="23ce2-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23ce2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="23ce2-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23ce2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="23ce2-108">DESCRIPTION</span></span>
<span data-ttu-id="23ce2-109">Bu aboneliğin güvenlik çalışma alanı ayarını siler.</span><span class="sxs-lookup"><span data-stu-id="23ce2-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="23ce2-110">Bu eylem, yeni yüklü güvenlik aracılarının bu aboneliğin varsayılan çalışma alanına raporlanmasını sağlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="23ce2-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="23ce2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23ce2-111">EXAMPLES</span></span>

### <span data-ttu-id="23ce2-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="23ce2-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="23ce2-113">Bu aboneliğin güvenlik çalışma alanı ayarını siler.</span><span class="sxs-lookup"><span data-stu-id="23ce2-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="23ce2-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23ce2-114">PARAMETERS</span></span>

### <span data-ttu-id="23ce2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23ce2-115">-DefaultProfile</span></span>
<span data-ttu-id="23ce2-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="23ce2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23ce2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23ce2-117">-InputObject</span></span>
<span data-ttu-id="23ce2-118">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="23ce2-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23ce2-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="23ce2-119">-Name</span></span>
<span data-ttu-id="23ce2-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="23ce2-120">Resource name.</span></span>

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

### <span data-ttu-id="23ce2-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="23ce2-121">-PassThru</span></span>
<span data-ttu-id="23ce2-122">İşlemin başarılı olup olmadığını döndürün.</span><span class="sxs-lookup"><span data-stu-id="23ce2-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="23ce2-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="23ce2-123">-ResourceId</span></span>
<span data-ttu-id="23ce2-124">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="23ce2-124">Resource ID.</span></span>

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

### <span data-ttu-id="23ce2-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="23ce2-125">-Confirm</span></span>
<span data-ttu-id="23ce2-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="23ce2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23ce2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23ce2-127">-WhatIf</span></span>
<span data-ttu-id="23ce2-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="23ce2-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23ce2-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="23ce2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23ce2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23ce2-130">CommonParameters</span></span>
<span data-ttu-id="23ce2-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23ce2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23ce2-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23ce2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23ce2-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23ce2-133">INPUTS</span></span>

### <span data-ttu-id="23ce2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="23ce2-134">System.String</span></span>

### <span data-ttu-id="23ce2-135">Microsoft. Azure. Commands. Security. model.</span><span class="sxs-lookup"><span data-stu-id="23ce2-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="23ce2-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23ce2-136">OUTPUTS</span></span>

### <span data-ttu-id="23ce2-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23ce2-137">System.Boolean</span></span>

## <span data-ttu-id="23ce2-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23ce2-138">NOTES</span></span>

## <span data-ttu-id="23ce2-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23ce2-139">RELATED LINKS</span></span>
