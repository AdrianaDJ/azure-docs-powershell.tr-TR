---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 679b1458b3e749b2ccfca3863f745edd562ffc2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759221"
---
# <span data-ttu-id="569b2-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="569b2-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="569b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="569b2-102">SYNOPSIS</span></span>
<span data-ttu-id="569b2-103">Aboneliğin çalışma alanı ayarlarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="569b2-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="569b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="569b2-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="569b2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="569b2-105">DESCRIPTION</span></span>
<span data-ttu-id="569b2-106">Aboneliğin çalışma alanı ayarlarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="569b2-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="569b2-107">Yapılandırılmış çalışma alanı, bu aboneliğin içindeki VM 'Ler 'e yüklenen güvenlik Aracısı tarafından toplanan güvenlik verilerini tutar.</span><span class="sxs-lookup"><span data-stu-id="569b2-107">The configured workspace will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="569b2-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="569b2-108">EXAMPLES</span></span>

### <span data-ttu-id="569b2-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="569b2-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="569b2-110">"MyWorkspace" çalışma alanını, güvenlik aracıları tarafından toplanan tüm güvenlik verilerini tutmak için ayarlar.</span><span class="sxs-lookup"><span data-stu-id="569b2-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the security agents.</span></span>

## <span data-ttu-id="569b2-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="569b2-111">PARAMETERS</span></span>

### <span data-ttu-id="569b2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="569b2-112">-DefaultProfile</span></span>
<span data-ttu-id="569b2-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="569b2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="569b2-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="569b2-114">-Name</span></span>
<span data-ttu-id="569b2-115">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="569b2-115">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="569b2-116">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="569b2-116">-Scope</span></span>
<span data-ttu-id="569b2-117">Yay.</span><span class="sxs-lookup"><span data-stu-id="569b2-117">Scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="569b2-118">-</span><span class="sxs-lookup"><span data-stu-id="569b2-118">-WorkspaceId</span></span>
<span data-ttu-id="569b2-119">Çalışma alanı KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="569b2-119">Workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="569b2-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="569b2-120">-Confirm</span></span>
<span data-ttu-id="569b2-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="569b2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="569b2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="569b2-122">-WhatIf</span></span>
<span data-ttu-id="569b2-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="569b2-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="569b2-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="569b2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="569b2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="569b2-125">CommonParameters</span></span>
<span data-ttu-id="569b2-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="569b2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="569b2-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="569b2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="569b2-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="569b2-128">INPUTS</span></span>

### <span data-ttu-id="569b2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="569b2-129">System.String</span></span>

## <span data-ttu-id="569b2-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="569b2-130">OUTPUTS</span></span>

### <span data-ttu-id="569b2-131">Microsoft. Azure. Commands. Security. model.</span><span class="sxs-lookup"><span data-stu-id="569b2-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="569b2-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="569b2-132">NOTES</span></span>

## <span data-ttu-id="569b2-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="569b2-133">RELATED LINKS</span></span>
