---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 1c6f6a38c1811bdda32b60d4af1707c78eb7afd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762581"
---
# <span data-ttu-id="9cdae-101">Remove-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="9cdae-101">Remove-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="9cdae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cdae-102">SYNOPSIS</span></span>
<span data-ttu-id="9cdae-103">Bu aboneliğin güvenlik çalışma alanı ayarını siler.</span><span class="sxs-lookup"><span data-stu-id="9cdae-103">Deletes the security workspace setting for this subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cdae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9cdae-104">SYNTAX</span></span>

### <span data-ttu-id="9cdae-105">SubscriptionLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9cdae-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cdae-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="9cdae-106">ResourceId</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cdae-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="9cdae-107">InputObject</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -InputObject <PSRemoveWorkspaceSettingInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cdae-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9cdae-108">DESCRIPTION</span></span>
<span data-ttu-id="9cdae-109">Bu aboneliğin güvenlik çalışma alanı ayarını siler.</span><span class="sxs-lookup"><span data-stu-id="9cdae-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="9cdae-110">Bu eylem, yeni yüklenmiş güvenlik aracılarının bu susma varsayılan çalışma alanına rapor yapmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="9cdae-110">This action will make the newly installed security agents to report to the default workspace of this susbscription.</span></span>

## <span data-ttu-id="9cdae-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9cdae-111">EXAMPLES</span></span>

### <span data-ttu-id="9cdae-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9cdae-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="9cdae-113">Bu aboneliğin güvenlik çalışma alanı ayarını siler.</span><span class="sxs-lookup"><span data-stu-id="9cdae-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="9cdae-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9cdae-114">PARAMETERS</span></span>

### <span data-ttu-id="9cdae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cdae-115">-DefaultProfile</span></span>
<span data-ttu-id="9cdae-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9cdae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cdae-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cdae-117">-InputObject</span></span>
<span data-ttu-id="9cdae-118">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9cdae-118">Input Object.</span></span>

```yaml
Type: PSRemoveWorkspaceSettingInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cdae-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="9cdae-119">-Name</span></span>
<span data-ttu-id="9cdae-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="9cdae-120">Resource name.</span></span>

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

### <span data-ttu-id="9cdae-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9cdae-121">-PassThru</span></span>
<span data-ttu-id="9cdae-122">İşlemin başarılı olup olmadığını döndürün.</span><span class="sxs-lookup"><span data-stu-id="9cdae-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="9cdae-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9cdae-123">-ResourceId</span></span>
<span data-ttu-id="9cdae-124">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="9cdae-124">Resource ID.</span></span>

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

### <span data-ttu-id="9cdae-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="9cdae-125">-Confirm</span></span>
<span data-ttu-id="9cdae-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9cdae-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cdae-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cdae-127">-WhatIf</span></span>
<span data-ttu-id="9cdae-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9cdae-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9cdae-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9cdae-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cdae-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cdae-130">CommonParameters</span></span>
<span data-ttu-id="9cdae-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9cdae-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cdae-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cdae-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cdae-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9cdae-133">INPUTS</span></span>

### <span data-ttu-id="9cdae-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9cdae-134">System.String</span></span>
<span data-ttu-id="9cdae-135">Microsoft. Azure. Commands. Security. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cdae-135">Microsoft.Azure.Commands.Security.Cmdlets.WorkspaceSettings.PSRemoveWorkspaceSettingInputObject</span></span>

## <span data-ttu-id="9cdae-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9cdae-136">OUTPUTS</span></span>

### <span data-ttu-id="9cdae-137">Microsoft. Azure. Commands. Security. model.</span><span class="sxs-lookup"><span data-stu-id="9cdae-137">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="9cdae-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9cdae-138">NOTES</span></span>

## <span data-ttu-id="9cdae-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9cdae-139">RELATED LINKS</span></span>
