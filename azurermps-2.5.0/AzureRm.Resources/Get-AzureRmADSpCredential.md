---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadspcredential
schema: 2.0.0
ms.openlocfilehash: a0f4c41b310e820b939500b8496b411d7b0266d1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939489"
---
# <span data-ttu-id="4c833-101">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="4c833-101">Get-AzureRmADSpCredential</span></span>

## <span data-ttu-id="4c833-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c833-102">SYNOPSIS</span></span>
<span data-ttu-id="4c833-103">Hizmet sorumlusu ile ilişkili kimlik bilgilerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="4c833-103">Retrieves a list of credentials associated with a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c833-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c833-104">SYNTAX</span></span>

### <span data-ttu-id="4c833-105">Objectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4c833-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADSpCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c833-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c833-106">SPNParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c833-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c833-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c833-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c833-108">SPNObjectParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c833-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c833-109">DESCRIPTION</span></span>
<span data-ttu-id="4c833-110">Hizmet sorumlusu ile ilişkili kimlik bilgilerinin listesini almak için Get-AzureRmADSpCredential cmdlet 'i kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4c833-110">The Get-AzureRmADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="4c833-111">Bu komut, hizmet sorumlusunun tüm kimlik bilgisi özelliklerini (ancak kimlik bilgisi değerini değil) alır.</span><span class="sxs-lookup"><span data-stu-id="4c833-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="4c833-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c833-112">EXAMPLES</span></span>

### <span data-ttu-id="4c833-113">Örnek 1-SPN 'ye göre liste kimlik bilgileri</span><span class="sxs-lookup"><span data-stu-id="4c833-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="4c833-114">SPN ile hizmet sorumlusunun ilişkili kimlik bilgileri listesini döndürür ' http://test12345 .</span><span class="sxs-lookup"><span data-stu-id="4c833-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="4c833-115">Örnek 2-nesne kimliğine göre liste kimlik bilgileri</span><span class="sxs-lookup"><span data-stu-id="4c833-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzureRmADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="4c833-116">Nesne kimliği "58e28616-99cc-4da4-b705-7672130e1047" ile hizmet sorumlusunun ilişkili kimlik bilgileri listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="4c833-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="4c833-117">Örnek 3-boru tarafından kimlik bilgileri</span><span class="sxs-lookup"><span data-stu-id="4c833-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzureRmADSpCredential
```

<span data-ttu-id="4c833-118">Hizmet sorumlusunu nesne kimliği "58e28616-99cc-4da4-b705-7672130e1047" ile alır ve bu hizmet sorumlusunun tüm kimlik bilgilerini listelemek için Get-AzureRmADSpCredential cmdlet 'ine yöneltin.</span><span class="sxs-lookup"><span data-stu-id="4c833-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzureRmADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="4c833-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c833-119">PARAMETERS</span></span>

### <span data-ttu-id="4c833-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c833-120">-DefaultProfile</span></span>
<span data-ttu-id="4c833-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4c833-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c833-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4c833-122">-DisplayName</span></span>
<span data-ttu-id="4c833-123">Hizmet sorumlusunun görünen adı</span><span class="sxs-lookup"><span data-stu-id="4c833-123">The display name of the service principal</span></span>

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

### <span data-ttu-id="4c833-124">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="4c833-124">-ObjectId</span></span>
<span data-ttu-id="4c833-125">Kimlik bilgilerinin alınacağı hizmet sorumlusunun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="4c833-125">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c833-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="4c833-126">-ServicePrincipalName</span></span>
<span data-ttu-id="4c833-127">Kimlik bilgilerinin alınacağı hizmet sorumlusunun adı (SPN).</span><span class="sxs-lookup"><span data-stu-id="4c833-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="4c833-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="4c833-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="4c833-129">Kimlik bilgilerini alacak hizmet sorumlusu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4c833-129">The service principal object to retrieve the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c833-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c833-130">CommonParameters</span></span>
<span data-ttu-id="4c833-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c833-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c833-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c833-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c833-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c833-133">INPUTS</span></span>

### <span data-ttu-id="4c833-134">System. Guid</span><span class="sxs-lookup"><span data-stu-id="4c833-134">System.Guid</span></span>

### <span data-ttu-id="4c833-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4c833-135">System.String</span></span>

### <span data-ttu-id="4c833-136">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4c833-136">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="4c833-137">Parametreler: ServicePrincipalObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4c833-137">Parameters: ServicePrincipalObject (ByValue)</span></span>

## <span data-ttu-id="4c833-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c833-138">OUTPUTS</span></span>

### <span data-ttu-id="4c833-139">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="4c833-139">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="4c833-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c833-140">NOTES</span></span>

## <span data-ttu-id="4c833-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c833-141">RELATED LINKS</span></span>

[<span data-ttu-id="4c833-142">Yeni-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="4c833-142">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="4c833-143">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="4c833-143">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="4c833-144">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4c833-144">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

