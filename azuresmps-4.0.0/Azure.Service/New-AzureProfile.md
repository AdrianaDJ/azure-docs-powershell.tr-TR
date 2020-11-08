---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 159CAD26-710A-4E65-B015-015A2C336A91
online version: ''
schema: 2.0.0
ms.openlocfilehash: a224ac58e6a8344953e29164de6ac6cfe0d00d97
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106000"
---
# <span data-ttu-id="eb151-101">New-AzureProfile</span><span class="sxs-lookup"><span data-stu-id="eb151-101">New-AzureProfile</span></span>

## <span data-ttu-id="eb151-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb151-102">SYNOPSIS</span></span>

## <span data-ttu-id="eb151-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eb151-103">SYNTAX</span></span>

### <span data-ttu-id="eb151-104">Sertifika</span><span class="sxs-lookup"><span data-stu-id="eb151-104">Certificate</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Certificate <X509Certificate2> [<CommonParameters>]
```

### <span data-ttu-id="eb151-105">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="eb151-105">ServicePrincipal</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Credential <PSCredential> -Tenant <String> [-ServicePrincipal] [<CommonParameters>]
```

### <span data-ttu-id="eb151-106">Belirteci</span><span class="sxs-lookup"><span data-stu-id="eb151-106">Token</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -AccessToken <String> -AccountId <String> [<CommonParameters>]
```

### <span data-ttu-id="eb151-107">Bilgilerini</span><span class="sxs-lookup"><span data-stu-id="eb151-107">Credentials</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Credential <PSCredential> [-Tenant <String>] [<CommonParameters>]
```

### <span data-ttu-id="eb151-108">Boşaltma</span><span class="sxs-lookup"><span data-stu-id="eb151-108">Empty</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] [<CommonParameters>]
```

### <span data-ttu-id="eb151-109">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="eb151-109">File</span></span>
```
New-AzureProfile -Path <String> [<CommonParameters>]
```

### <span data-ttu-id="eb151-110">PropertyBag</span><span class="sxs-lookup"><span data-stu-id="eb151-110">PropertyBag</span></span>
```
New-AzureProfile -Properties <Hashtable> [<CommonParameters>]
```

## <span data-ttu-id="eb151-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="eb151-111">DESCRIPTION</span></span>

## <span data-ttu-id="eb151-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eb151-112">EXAMPLES</span></span>

### <span data-ttu-id="eb151-113">2</span><span class="sxs-lookup"><span data-stu-id="eb151-113">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="eb151-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eb151-114">PARAMETERS</span></span>

### <span data-ttu-id="eb151-115">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="eb151-115">-AccessToken</span></span>
```yaml
Type: String
Parameter Sets: Token
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb151-116">-AccountId</span><span class="sxs-lookup"><span data-stu-id="eb151-116">-AccountId</span></span>
```yaml
Type: String
Parameter Sets: Token
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb151-117">-Sertifika</span><span class="sxs-lookup"><span data-stu-id="eb151-117">-Certificate</span></span>
```yaml
Type: X509Certificate2
Parameter Sets: Certificate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb151-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="eb151-118">-Credential</span></span>
```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal, Credentials
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb151-119">-Ortam</span><span class="sxs-lookup"><span data-stu-id="eb151-119">-Environment</span></span>
```yaml
Type: AzureEnvironment
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials, Empty
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb151-120">-Yol</span><span class="sxs-lookup"><span data-stu-id="eb151-120">-Path</span></span>
```yaml
Type: String
Parameter Sets: File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb151-121">-Özellikler</span><span class="sxs-lookup"><span data-stu-id="eb151-121">-Properties</span></span>
```yaml
Type: Hashtable
Parameter Sets: PropertyBag
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb151-122">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="eb151-122">-ServicePrincipal</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb151-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="eb151-123">-StorageAccount</span></span>
```yaml
Type: String
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb151-124">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="eb151-124">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb151-125">-Tenant</span><span class="sxs-lookup"><span data-stu-id="eb151-125">-Tenant</span></span>
```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Credentials
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb151-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb151-126">CommonParameters</span></span>
<span data-ttu-id="eb151-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eb151-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb151-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb151-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb151-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eb151-129">INPUTS</span></span>

## <span data-ttu-id="eb151-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eb151-130">OUTPUTS</span></span>

## <span data-ttu-id="eb151-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eb151-131">NOTES</span></span>

## <span data-ttu-id="eb151-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eb151-132">RELATED LINKS</span></span>

