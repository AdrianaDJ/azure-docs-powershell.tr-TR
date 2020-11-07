---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
ms.openlocfilehash: 1f9f0258bf107ae0ca7be7050f8db8e3db8b1ffa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752215"
---
# <span data-ttu-id="afab9-101">Get-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="afab9-101">Get-AzDataShareInvitation</span></span>

## <span data-ttu-id="afab9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afab9-102">SYNOPSIS</span></span>
<span data-ttu-id="afab9-103">Veri paylaşımının bilgi davetini alır.</span><span class="sxs-lookup"><span data-stu-id="afab9-103">Gets information invitation of data share.</span></span>

## <span data-ttu-id="afab9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="afab9-104">SYNTAX</span></span>

### <span data-ttu-id="afab9-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="afab9-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afab9-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="afab9-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareInvitation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afab9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="afab9-107">DESCRIPTION</span></span>
<span data-ttu-id="afab9-108">**Get-Azdatasharedavetcmdlet** 'i veri paylaşımında bulunan davetlerde bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="afab9-108">The **Get-AzDataShareInvitation** cmdlet gets information on invitations added in data share.</span></span> <span data-ttu-id="afab9-109">Davetin adını belirtirseniz, bu cmdlet davet hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="afab9-109">If you specify the name of the invitation, this cmdlet gets information about the invitation.</span></span> <span data-ttu-id="afab9-110">Bir ad belirtmezseniz, bu cmdlet paylaşımdaki tüm davetler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="afab9-110">If you do not specify a name, this cmdlet gets information about all the invitations in a share.</span></span>

## <span data-ttu-id="afab9-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="afab9-111">EXAMPLES</span></span>

### <span data-ttu-id="afab9-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="afab9-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation"

InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

<span data-ttu-id="afab9-113">Bu komut, veri paylaşımı AdsShare ile ilgili davet etme hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="afab9-113">This commands provides information about invitation AdsInvitation present in data share AdsShare.</span></span>

## <span data-ttu-id="afab9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="afab9-114">PARAMETERS</span></span>

### <span data-ttu-id="afab9-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="afab9-115">-AccountName</span></span>
<span data-ttu-id="afab9-116">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="afab9-116">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afab9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afab9-117">-DefaultProfile</span></span>
<span data-ttu-id="afab9-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="afab9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afab9-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="afab9-119">-Name</span></span>
<span data-ttu-id="afab9-120">Azure veri paylaşımı davet adı</span><span class="sxs-lookup"><span data-stu-id="afab9-120">Azure data share invitation name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afab9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afab9-121">-ResourceGroupName</span></span>
<span data-ttu-id="afab9-122">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="afab9-122">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afab9-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="afab9-123">-ResourceId</span></span>
<span data-ttu-id="afab9-124">Azure veri paylaşımı davetinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="afab9-124">The resource id of the azure data share invitation</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afab9-125">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="afab9-125">-ShareName</span></span>
<span data-ttu-id="afab9-126">Azure veri paylaşımı adı</span><span class="sxs-lookup"><span data-stu-id="afab9-126">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afab9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afab9-127">CommonParameters</span></span>
<span data-ttu-id="afab9-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="afab9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afab9-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afab9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afab9-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="afab9-130">INPUTS</span></span>

### <span data-ttu-id="afab9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="afab9-131">System.String</span></span>

## <span data-ttu-id="afab9-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="afab9-132">OUTPUTS</span></span>

### <span data-ttu-id="afab9-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDAtapaylaşımı</span><span class="sxs-lookup"><span data-stu-id="afab9-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="afab9-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="afab9-134">NOTES</span></span>

## <span data-ttu-id="afab9-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="afab9-135">RELATED LINKS</span></span>