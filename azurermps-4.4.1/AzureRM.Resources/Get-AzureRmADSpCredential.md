---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
ms.openlocfilehash: 247b0735e41f02a55b94e5a8f8ed44136eb3f37e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587802"
---
# <span data-ttu-id="a1138-101">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a1138-101">Get-AzureRmADSpCredential</span></span>

## <span data-ttu-id="a1138-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1138-102">SYNOPSIS</span></span>
<span data-ttu-id="a1138-103">Hizmet sorumlusu ile ilişkili kimlik bilgilerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="a1138-103">Retrieves a list of credentials associated with a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1138-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1138-104">SYNTAX</span></span>

### <span data-ttu-id="a1138-105">Objectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a1138-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1138-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1138-106">SPNParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1138-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1138-107">DESCRIPTION</span></span>
<span data-ttu-id="a1138-108">Hizmet sorumlusu ile ilişkili kimlik bilgilerinin listesini almak için Get-AzureRmADSpCredential cmdlet 'i kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a1138-108">The Get-AzureRmADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="a1138-109">Bu komut, hizmet sorumlusunun tüm kimlik bilgisi özelliklerini (ancak kimlik bilgisi değerini değil) alır.</span><span class="sxs-lookup"><span data-stu-id="a1138-109">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="a1138-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1138-110">EXAMPLES</span></span>

### <span data-ttu-id="a1138-111">--------------------------Örnek 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a1138-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="a1138-112">SPN sahibi olan hizmet sorumlusunun ilişkili kimlik bilgileri listesini döndürür http://test12345 .</span><span class="sxs-lookup"><span data-stu-id="a1138-112">Returns a list of credentials associated with the service principal having SPN 'http://test12345'.</span></span>

## <span data-ttu-id="a1138-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1138-113">PARAMETERS</span></span>

### <span data-ttu-id="a1138-114">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="a1138-114">-ObjectId</span></span>
<span data-ttu-id="a1138-115">Kimlik bilgilerinin alınacağı hizmet sorumlusunun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="a1138-115">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1138-116">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a1138-116">-ServicePrincipalName</span></span>
<span data-ttu-id="a1138-117">Kimlik bilgilerinin alınacağı hizmet sorumlusunun adı (SPN).</span><span class="sxs-lookup"><span data-stu-id="a1138-117">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1138-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1138-118">-DefaultProfile</span></span>
<span data-ttu-id="a1138-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a1138-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1138-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1138-120">CommonParameters</span></span>
<span data-ttu-id="a1138-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1138-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1138-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1138-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1138-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1138-123">INPUTS</span></span>

## <span data-ttu-id="a1138-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1138-124">OUTPUTS</span></span>

### <span data-ttu-id="a1138-125">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="a1138-125">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="a1138-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1138-126">NOTES</span></span>

## <span data-ttu-id="a1138-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1138-127">RELATED LINKS</span></span>

[<span data-ttu-id="a1138-128">Yeni-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a1138-128">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="a1138-129">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a1138-129">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="a1138-130">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a1138-130">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

