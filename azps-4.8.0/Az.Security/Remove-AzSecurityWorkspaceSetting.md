---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 75e68cfac55c8fb7086f02d5e70dc466f335d1de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266371"
---
# <span data-ttu-id="d74d0-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="d74d0-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="d74d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d74d0-102">SYNOPSIS</span></span>
<span data-ttu-id="d74d0-103">Bu aboneliğin güvenlik çalışma alanı ayarını siler.</span><span class="sxs-lookup"><span data-stu-id="d74d0-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="d74d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d74d0-104">SYNTAX</span></span>

### <span data-ttu-id="d74d0-105">SubscriptionLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d74d0-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d74d0-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="d74d0-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d74d0-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d74d0-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d74d0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d74d0-108">DESCRIPTION</span></span>
<span data-ttu-id="d74d0-109">Bu aboneliğin güvenlik çalışma alanı ayarını siler.</span><span class="sxs-lookup"><span data-stu-id="d74d0-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="d74d0-110">Bu eylem, yeni yüklü güvenlik aracılarının bu aboneliğin varsayılan çalışma alanına raporlanmasını sağlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="d74d0-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="d74d0-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d74d0-111">EXAMPLES</span></span>

### <span data-ttu-id="d74d0-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d74d0-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="d74d0-113">Bu aboneliğin güvenlik çalışma alanı ayarını siler.</span><span class="sxs-lookup"><span data-stu-id="d74d0-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="d74d0-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d74d0-114">PARAMETERS</span></span>

### <span data-ttu-id="d74d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d74d0-115">-DefaultProfile</span></span>
<span data-ttu-id="d74d0-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d74d0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d74d0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d74d0-117">-InputObject</span></span>
<span data-ttu-id="d74d0-118">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d74d0-118">Input Object.</span></span>

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

### <span data-ttu-id="d74d0-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d74d0-119">-Name</span></span>
<span data-ttu-id="d74d0-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="d74d0-120">Resource name.</span></span>

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

### <span data-ttu-id="d74d0-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d74d0-121">-PassThru</span></span>
<span data-ttu-id="d74d0-122">İşlemin başarılı olup olmadığını döndürün.</span><span class="sxs-lookup"><span data-stu-id="d74d0-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="d74d0-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d74d0-123">-ResourceId</span></span>
<span data-ttu-id="d74d0-124">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d74d0-124">Resource ID.</span></span>

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

### <span data-ttu-id="d74d0-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="d74d0-125">-Confirm</span></span>
<span data-ttu-id="d74d0-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d74d0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d74d0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d74d0-127">-WhatIf</span></span>
<span data-ttu-id="d74d0-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d74d0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d74d0-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d74d0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d74d0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d74d0-130">CommonParameters</span></span>
<span data-ttu-id="d74d0-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d74d0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d74d0-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d74d0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d74d0-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d74d0-133">INPUTS</span></span>

### <span data-ttu-id="d74d0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d74d0-134">System.String</span></span>

### <span data-ttu-id="d74d0-135">Microsoft. Azure. Commands. Security. model.</span><span class="sxs-lookup"><span data-stu-id="d74d0-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="d74d0-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d74d0-136">OUTPUTS</span></span>

### <span data-ttu-id="d74d0-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d74d0-137">System.Boolean</span></span>

## <span data-ttu-id="d74d0-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d74d0-138">NOTES</span></span>

## <span data-ttu-id="d74d0-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d74d0-139">RELATED LINKS</span></span>
