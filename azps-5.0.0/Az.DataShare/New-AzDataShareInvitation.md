---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
ms.openlocfilehash: ea042cb0db8fcb1995a935086d188efbb6c0647f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320294"
---
# <span data-ttu-id="a7a01-101">New-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="a7a01-101">New-AzDataShareInvitation</span></span>

## <span data-ttu-id="a7a01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7a01-102">SYNOPSIS</span></span>
<span data-ttu-id="a7a01-103">Paylaşım için bir davet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a7a01-103">Creates an invitation for share.</span></span>

## <span data-ttu-id="a7a01-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7a01-104">SYNTAX</span></span>

### <span data-ttu-id="a7a01-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a7a01-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareInvitation [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7a01-106">Bydavetiemailparameterset</span><span class="sxs-lookup"><span data-stu-id="a7a01-106">ByInvitationEmailParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetEmail <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7a01-107">Bydavetitenantparameterset</span><span class="sxs-lookup"><span data-stu-id="a7a01-107">ByInvitationTenantParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetObjectId <String> -TargetTenantId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7a01-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7a01-108">DESCRIPTION</span></span>
<span data-ttu-id="a7a01-109">**New-Azdatasharedavetiye** cmdlet 'i hedef tüketiciye sağlayıcı paylaşımı hakkında bilgi içeren bir davet gönderir.</span><span class="sxs-lookup"><span data-stu-id="a7a01-109">The **New-AzDataShareInvitation** cmdlet sends an invitation to the target consumer with information about the provider share.</span></span> 

## <span data-ttu-id="a7a01-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7a01-110">EXAMPLES</span></span>

### <span data-ttu-id="a7a01-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a7a01-111">Example 1</span></span>
```
PS C:\> New-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation" -TargetEmail "adstest@microsoft.com"
InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/        providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

<span data-ttu-id="a7a01-112">Bu komut, Share AdsShare için bir davet adstest@microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a7a01-112">This command creates an invitation AdsInvitation for share AdsShare and sends it to target email adstest@microsoft.com.</span></span>

## <span data-ttu-id="a7a01-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7a01-113">PARAMETERS</span></span>

### <span data-ttu-id="a7a01-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a7a01-114">-AccountName</span></span>
<span data-ttu-id="a7a01-115">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="a7a01-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7a01-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7a01-116">-DefaultProfile</span></span>
<span data-ttu-id="a7a01-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a7a01-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7a01-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="a7a01-118">-Name</span></span>
<span data-ttu-id="a7a01-119">Azure veri paylaşımı davet adı</span><span class="sxs-lookup"><span data-stu-id="a7a01-119">Azure data share invitation name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7a01-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7a01-120">-ResourceGroupName</span></span>
<span data-ttu-id="a7a01-121">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a7a01-121">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7a01-122">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="a7a01-122">-ShareName</span></span>
<span data-ttu-id="a7a01-123">Azure veri paylaşımı adı</span><span class="sxs-lookup"><span data-stu-id="a7a01-123">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7a01-124">-TargetEmail</span><span class="sxs-lookup"><span data-stu-id="a7a01-124">-TargetEmail</span></span>
<span data-ttu-id="a7a01-125">Hedef e-posta kimliği</span><span class="sxs-lookup"><span data-stu-id="a7a01-125">Target email id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7a01-126">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="a7a01-126">-TargetObjectId</span></span>
<span data-ttu-id="a7a01-127">Hedef nesne kimliği</span><span class="sxs-lookup"><span data-stu-id="a7a01-127">Target object id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7a01-128">-Targettenantıd</span><span class="sxs-lookup"><span data-stu-id="a7a01-128">-TargetTenantId</span></span>
<span data-ttu-id="a7a01-129">Hedef Kiracı kimliği</span><span class="sxs-lookup"><span data-stu-id="a7a01-129">Target tenant id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7a01-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="a7a01-130">-Confirm</span></span>
<span data-ttu-id="a7a01-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a7a01-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7a01-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7a01-132">-WhatIf</span></span>
<span data-ttu-id="a7a01-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a7a01-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7a01-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a7a01-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7a01-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7a01-135">CommonParameters</span></span>
<span data-ttu-id="a7a01-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7a01-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7a01-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a7a01-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7a01-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7a01-138">INPUTS</span></span>

### <span data-ttu-id="a7a01-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a7a01-139">None</span></span>

## <span data-ttu-id="a7a01-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7a01-140">OUTPUTS</span></span>

### <span data-ttu-id="a7a01-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDAtapaylaşıdavetiyesi</span><span class="sxs-lookup"><span data-stu-id="a7a01-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="a7a01-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7a01-142">NOTES</span></span>

## <span data-ttu-id="a7a01-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7a01-143">RELATED LINKS</span></span>
