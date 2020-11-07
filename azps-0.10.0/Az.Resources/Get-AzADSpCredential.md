---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: 40543468145c7fcfaf49fcfc7cad1cbf70938adf
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936458"
---
# <span data-ttu-id="cbad6-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="cbad6-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="cbad6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbad6-102">SYNOPSIS</span></span>
<span data-ttu-id="cbad6-103">Hizmet sorumlusu ile ilişkili kimlik bilgilerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="cbad6-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="cbad6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cbad6-104">SYNTAX</span></span>

### <span data-ttu-id="cbad6-105">Objectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cbad6-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbad6-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbad6-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cbad6-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbad6-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbad6-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbad6-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbad6-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="cbad6-109">DESCRIPTION</span></span>
<span data-ttu-id="cbad6-110">Hizmet sorumlusu ile ilişkili kimlik bilgilerinin listesini almak için Get-AzADSpCredential cmdlet 'i kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="cbad6-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="cbad6-111">Bu komut, hizmet sorumlusunun tüm kimlik bilgisi özelliklerini (ancak kimlik bilgisi değerini değil) alır.</span><span class="sxs-lookup"><span data-stu-id="cbad6-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="cbad6-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cbad6-112">EXAMPLES</span></span>

### <span data-ttu-id="cbad6-113">Örnek 1-SPN 'ye göre liste kimlik bilgileri</span><span class="sxs-lookup"><span data-stu-id="cbad6-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="cbad6-114">SPN ile hizmet sorumlusunun ilişkili kimlik bilgileri listesini döndürür ' http://test12345 .</span><span class="sxs-lookup"><span data-stu-id="cbad6-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="cbad6-115">Örnek 2-nesne kimliğine göre liste kimlik bilgileri</span><span class="sxs-lookup"><span data-stu-id="cbad6-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="cbad6-116">Nesne kimliği "58e28616-99cc-4da4-b705-7672130e1047" ile hizmet sorumlusunun ilişkili kimlik bilgileri listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="cbad6-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="cbad6-117">Örnek 3-boru tarafından kimlik bilgileri</span><span class="sxs-lookup"><span data-stu-id="cbad6-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="cbad6-118">Hizmet sorumlusunu nesne kimliği "58e28616-99cc-4da4-b705-7672130e1047" ile alır ve bu hizmet sorumlusunun tüm kimlik bilgilerini listelemek için Get-AzADSpCredential cmdlet 'ine yöneltin.</span><span class="sxs-lookup"><span data-stu-id="cbad6-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="cbad6-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cbad6-119">PARAMETERS</span></span>

### <span data-ttu-id="cbad6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbad6-120">-DefaultProfile</span></span>
<span data-ttu-id="cbad6-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cbad6-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbad6-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cbad6-122">-DisplayName</span></span>
<span data-ttu-id="cbad6-123">Hizmet sorumlusunun görünen adı</span><span class="sxs-lookup"><span data-stu-id="cbad6-123">The display name of the service principal</span></span>

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

### <span data-ttu-id="cbad6-124">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="cbad6-124">-ObjectId</span></span>
<span data-ttu-id="cbad6-125">Kimlik bilgilerinin alınacağı hizmet sorumlusunun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="cbad6-125">The object id of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="cbad6-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="cbad6-126">-ServicePrincipalName</span></span>
<span data-ttu-id="cbad6-127">Kimlik bilgilerinin alınacağı hizmet sorumlusunun adı (SPN).</span><span class="sxs-lookup"><span data-stu-id="cbad6-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="cbad6-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="cbad6-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="cbad6-129">Kimlik bilgilerini alacak hizmet sorumlusu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="cbad6-129">The service principal object to retrieve the credentials from.</span></span>

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

### <span data-ttu-id="cbad6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbad6-130">CommonParameters</span></span>
<span data-ttu-id="cbad6-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cbad6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbad6-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbad6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbad6-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cbad6-133">INPUTS</span></span>

### <span data-ttu-id="cbad6-134">System. Guid</span><span class="sxs-lookup"><span data-stu-id="cbad6-134">System.Guid</span></span>

### <span data-ttu-id="cbad6-135">System. String</span><span class="sxs-lookup"><span data-stu-id="cbad6-135">System.String</span></span>

### <span data-ttu-id="cbad6-136">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="cbad6-136">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="cbad6-137">Parametreler: ServicePrincipalObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cbad6-137">Parameters: ServicePrincipalObject (ByValue)</span></span>

## <span data-ttu-id="cbad6-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cbad6-138">OUTPUTS</span></span>

### <span data-ttu-id="cbad6-139">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="cbad6-139">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="cbad6-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cbad6-140">NOTES</span></span>

## <span data-ttu-id="cbad6-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cbad6-141">RELATED LINKS</span></span>

[<span data-ttu-id="cbad6-142">Yeni-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="cbad6-142">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="cbad6-143">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="cbad6-143">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="cbad6-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="cbad6-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

