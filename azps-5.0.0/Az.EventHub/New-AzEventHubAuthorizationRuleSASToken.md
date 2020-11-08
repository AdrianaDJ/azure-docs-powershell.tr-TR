---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
ms.openlocfilehash: 24348c44ef9b529507c50a689f181739d1474e22
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278681"
---
# <span data-ttu-id="323ed-101">New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="323ed-101">New-AzEventHubAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="323ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="323ed-102">SYNOPSIS</span></span>
<span data-ttu-id="323ed-103">Ad alanı/eventhub için Azure eventhub yetkilendirme kuralı için SAS belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="323ed-103">Generates a SAS token for Azure eventhub authorization rule of namespace/eventhub.</span></span> 

## <span data-ttu-id="323ed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="323ed-104">SYNTAX</span></span>

```
New-AzEventHubAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="323ed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="323ed-105">DESCRIPTION</span></span>
<span data-ttu-id="323ed-106">New-AzEventHubAuthorizationRuleSASToken cmdlet 'i Azure Eventhub ad sapce veya Azure Eventhub için paylaşılan bir erişim Imzası (SAS) belirteci oluşturur</span><span class="sxs-lookup"><span data-stu-id="323ed-106">The New-AzEventHubAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="323ed-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="323ed-107">EXAMPLES</span></span>

### <span data-ttu-id="323ed-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="323ed-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="323ed-109">Başlangıç ve bitiş tarihi olan ad alanı için verilen authorixation kuralı için SAS belirteci oluştur..</span><span class="sxs-lookup"><span data-stu-id="323ed-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="323ed-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="323ed-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="323ed-111">Son kullanma tarihi olan ad alanı için verilen authorixation kuralı için SAS belirteci oluşturun.</span><span class="sxs-lookup"><span data-stu-id="323ed-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="323ed-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="323ed-112">PARAMETERS</span></span>

### <span data-ttu-id="323ed-113">-Authorizationruleıd</span><span class="sxs-lookup"><span data-stu-id="323ed-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="323ed-114">Yetki kuralının KOLUNU</span><span class="sxs-lookup"><span data-stu-id="323ed-114">ARM ResourceId of the Authoraization Rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="323ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="323ed-115">-DefaultProfile</span></span>
<span data-ttu-id="323ed-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="323ed-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="323ed-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="323ed-117">-ExpiryTime</span></span>
<span data-ttu-id="323ed-118">Son kullanma tarihi</span><span class="sxs-lookup"><span data-stu-id="323ed-118">Expiry Time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="323ed-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="323ed-119">-KeyType</span></span>
<span data-ttu-id="323ed-120">Anahtar türü</span><span class="sxs-lookup"><span data-stu-id="323ed-120">Key Type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="323ed-121">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="323ed-121">-StartTime</span></span>
<span data-ttu-id="323ed-122">Başlangıç saati</span><span class="sxs-lookup"><span data-stu-id="323ed-122">Start Time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="323ed-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="323ed-123">-Confirm</span></span>
<span data-ttu-id="323ed-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="323ed-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="323ed-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="323ed-125">-WhatIf</span></span>
<span data-ttu-id="323ed-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="323ed-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="323ed-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="323ed-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="323ed-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="323ed-128">CommonParameters</span></span>
<span data-ttu-id="323ed-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="323ed-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="323ed-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="323ed-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="323ed-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="323ed-131">INPUTS</span></span>

### <span data-ttu-id="323ed-132">System. String</span><span class="sxs-lookup"><span data-stu-id="323ed-132">System.String</span></span>

### <span data-ttu-id="323ed-133">System. Nullable ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="323ed-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="323ed-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="323ed-134">OUTPUTS</span></span>

### <span data-ttu-id="323ed-135">Microsoft. Azure. Commands. EventHub. modeller. Pssharedaccesstifreattributes</span><span class="sxs-lookup"><span data-stu-id="323ed-135">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="323ed-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="323ed-136">NOTES</span></span>

## <span data-ttu-id="323ed-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="323ed-137">RELATED LINKS</span></span>
