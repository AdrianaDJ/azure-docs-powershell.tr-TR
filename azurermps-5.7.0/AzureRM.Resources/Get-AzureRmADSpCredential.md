---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
ms.openlocfilehash: 8c03dd19fd2995347a3b4ae52de04fdcb3f02c30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762844"
---
# <span data-ttu-id="43838-101">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="43838-101">Get-AzureRmADSpCredential</span></span>

## <span data-ttu-id="43838-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43838-102">SYNOPSIS</span></span>
<span data-ttu-id="43838-103">Hizmet sorumlusu ile ilişkili kimlik bilgilerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="43838-103">Retrieves a list of credentials associated with a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43838-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="43838-104">SYNTAX</span></span>

### <span data-ttu-id="43838-105">Objectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="43838-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43838-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="43838-106">SPNParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43838-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="43838-107">DESCRIPTION</span></span>
<span data-ttu-id="43838-108">Hizmet sorumlusu ile ilişkili kimlik bilgilerinin listesini almak için Get-AzureRmADSpCredential cmdlet 'i kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="43838-108">The Get-AzureRmADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="43838-109">Bu komut, hizmet sorumlusunun tüm kimlik bilgisi özelliklerini (ancak kimlik bilgisi değerini değil) alır.</span><span class="sxs-lookup"><span data-stu-id="43838-109">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="43838-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="43838-110">EXAMPLES</span></span>

### <span data-ttu-id="43838-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="43838-111">Example 1</span></span>
```
PS E:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="43838-112">SPN sahibi olan hizmet sorumlusunun ilişkili kimlik bilgileri listesini döndürür http://test12345 .</span><span class="sxs-lookup"><span data-stu-id="43838-112">Returns a list of credentials associated with the service principal having SPN 'http://test12345'.</span></span>

## <span data-ttu-id="43838-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="43838-113">PARAMETERS</span></span>

### <span data-ttu-id="43838-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43838-114">-DefaultProfile</span></span>
<span data-ttu-id="43838-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="43838-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43838-116">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="43838-116">-ObjectId</span></span>
<span data-ttu-id="43838-117">Kimlik bilgilerinin alınacağı hizmet sorumlusunun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="43838-117">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43838-118">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="43838-118">-ServicePrincipalName</span></span>
<span data-ttu-id="43838-119">Kimlik bilgilerinin alınacağı hizmet sorumlusunun adı (SPN).</span><span class="sxs-lookup"><span data-stu-id="43838-119">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43838-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43838-120">CommonParameters</span></span>
<span data-ttu-id="43838-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="43838-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43838-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43838-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43838-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="43838-123">INPUTS</span></span>

### <span data-ttu-id="43838-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="43838-124">None</span></span>
<span data-ttu-id="43838-125">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="43838-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="43838-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="43838-126">OUTPUTS</span></span>

### <span data-ttu-id="43838-127">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="43838-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="43838-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="43838-128">NOTES</span></span>

## <span data-ttu-id="43838-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="43838-129">RELATED LINKS</span></span>

[<span data-ttu-id="43838-130">Yeni-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="43838-130">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="43838-131">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="43838-131">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="43838-132">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="43838-132">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

