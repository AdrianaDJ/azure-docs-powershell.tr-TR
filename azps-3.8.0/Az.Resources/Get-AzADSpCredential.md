---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: c22643c4ce47fc59d2640a6dbbdf9c15b0846f98
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938128"
---
# <span data-ttu-id="262a2-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="262a2-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="262a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="262a2-102">SYNOPSIS</span></span>
<span data-ttu-id="262a2-103">Hizmet sorumlusu ile ilişkili kimlik bilgilerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="262a2-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="262a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="262a2-104">SYNTAX</span></span>

### <span data-ttu-id="262a2-105">Objectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="262a2-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="262a2-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="262a2-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="262a2-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="262a2-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="262a2-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="262a2-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="262a2-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="262a2-109">DESCRIPTION</span></span>
<span data-ttu-id="262a2-110">Hizmet sorumlusu ile ilişkili kimlik bilgilerinin listesini almak için Get-AzADSpCredential cmdlet 'i kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="262a2-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="262a2-111">Bu komut, hizmet sorumlusunun tüm kimlik bilgisi özelliklerini (ancak kimlik bilgisi değerini değil) alır.</span><span class="sxs-lookup"><span data-stu-id="262a2-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="262a2-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="262a2-112">EXAMPLES</span></span>

### <span data-ttu-id="262a2-113">Örnek 1-SPN 'ye göre liste kimlik bilgileri</span><span class="sxs-lookup"><span data-stu-id="262a2-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="262a2-114">SPN ile hizmet sorumlusunun ilişkili kimlik bilgileri listesini döndürür ' http://test12345 .</span><span class="sxs-lookup"><span data-stu-id="262a2-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="262a2-115">Örnek 2-nesne kimliğine göre liste kimlik bilgileri</span><span class="sxs-lookup"><span data-stu-id="262a2-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="262a2-116">Nesne kimliği "58e28616-99cc-4da4-b705-7672130e1047" ile hizmet sorumlusunun ilişkili kimlik bilgileri listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="262a2-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="262a2-117">Örnek 3-boru tarafından kimlik bilgileri</span><span class="sxs-lookup"><span data-stu-id="262a2-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="262a2-118">Hizmet sorumlusunu nesne kimliği "58e28616-99cc-4da4-b705-7672130e1047" ile alır ve bu hizmet sorumlusunun tüm kimlik bilgilerini listelemek için Get-AzADSpCredential cmdlet 'ine yöneltin.</span><span class="sxs-lookup"><span data-stu-id="262a2-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="262a2-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="262a2-119">PARAMETERS</span></span>

### <span data-ttu-id="262a2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="262a2-120">-DefaultProfile</span></span>
<span data-ttu-id="262a2-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="262a2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="262a2-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="262a2-122">-DisplayName</span></span>
<span data-ttu-id="262a2-123">Hizmet sorumlusunun görünen adı</span><span class="sxs-lookup"><span data-stu-id="262a2-123">The display name of the service principal</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="262a2-124">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="262a2-124">-ObjectId</span></span>
<span data-ttu-id="262a2-125">Kimlik bilgilerinin alınacağı hizmet sorumlusunun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="262a2-125">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="262a2-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="262a2-126">-ServicePrincipalName</span></span>
<span data-ttu-id="262a2-127">Kimlik bilgilerinin alınacağı hizmet sorumlusunun adı (SPN).</span><span class="sxs-lookup"><span data-stu-id="262a2-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="262a2-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="262a2-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="262a2-129">Kimlik bilgilerini alacak hizmet sorumlusu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="262a2-129">The service principal object to retrieve the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="262a2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="262a2-130">CommonParameters</span></span>
<span data-ttu-id="262a2-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="262a2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="262a2-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="262a2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="262a2-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="262a2-133">INPUTS</span></span>

### <span data-ttu-id="262a2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="262a2-134">System.String</span></span>

### <span data-ttu-id="262a2-135">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="262a2-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="262a2-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="262a2-136">OUTPUTS</span></span>

### <span data-ttu-id="262a2-137">Microsoft. Azure. Commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="262a2-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="262a2-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="262a2-138">NOTES</span></span>

## <span data-ttu-id="262a2-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="262a2-139">RELATED LINKS</span></span>

[<span data-ttu-id="262a2-140">Yeni-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="262a2-140">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="262a2-141">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="262a2-141">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="262a2-142">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="262a2-142">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

