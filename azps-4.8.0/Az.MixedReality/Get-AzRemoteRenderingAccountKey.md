---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: e9397a2a62ebaa4d26e0d36aaad3fbe03bad137e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109946"
---
# <span data-ttu-id="e66a7-101">Get-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="e66a7-101">Get-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="e66a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e66a7-102">SYNOPSIS</span></span>
<span data-ttu-id="e66a7-103">Uzaktan Işleme hesabı anahtarlarını alma</span><span class="sxs-lookup"><span data-stu-id="e66a7-103">Get keys of Remote Rendering Account</span></span>

## <span data-ttu-id="e66a7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e66a7-104">SYNTAX</span></span>

### <span data-ttu-id="e66a7-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e66a7-105">DefaultParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e66a7-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e66a7-106">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e66a7-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="e66a7-107">PipelineParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e66a7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e66a7-108">DESCRIPTION</span></span>
<span data-ttu-id="e66a7-109">Uzaktan Işleme hesabı için geliştirici anahtarları edinin.</span><span class="sxs-lookup"><span data-stu-id="e66a7-109">Get developer keys of Remote Rendering Account.</span></span>

## <span data-ttu-id="e66a7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e66a7-110">EXAMPLES</span></span>

### <span data-ttu-id="e66a7-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e66a7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="e66a7-112">Geçerli aboneliğin ve "RG1" kaynak grubundan "örnek" uzaktan Işleme hesaplarının geliştirici anahtarlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="e66a7-112">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="e66a7-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e66a7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | Get-AzRemoteRenderingAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="e66a7-114">Geçerli abonelikten "örnek" uzaktan Işleme hesabı ve "RG1" kaynak grubundan yöneltme ile geliştirici anahtarları edinin.</span><span class="sxs-lookup"><span data-stu-id="e66a7-114">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="e66a7-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e66a7-115">PARAMETERS</span></span>

### <span data-ttu-id="e66a7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e66a7-116">-DefaultProfile</span></span>
<span data-ttu-id="e66a7-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e66a7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e66a7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e66a7-118">-InputObject</span></span>
<span data-ttu-id="e66a7-119">Özel etki alanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e66a7-119">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e66a7-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="e66a7-120">-Name</span></span>
<span data-ttu-id="e66a7-121">Uzaktan Işleme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="e66a7-121">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e66a7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e66a7-122">-ResourceGroupName</span></span>
<span data-ttu-id="e66a7-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e66a7-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e66a7-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e66a7-124">-ResourceId</span></span>
<span data-ttu-id="e66a7-125">Uzaktan Işleme hesabı kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e66a7-125">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e66a7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e66a7-126">CommonParameters</span></span>
<span data-ttu-id="e66a7-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e66a7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e66a7-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e66a7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e66a7-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e66a7-129">INPUTS</span></span>

### <span data-ttu-id="e66a7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e66a7-130">System.String</span></span>

### <span data-ttu-id="e66a7-131">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="e66a7-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="e66a7-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e66a7-132">OUTPUTS</span></span>

### <span data-ttu-id="e66a7-133">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e66a7-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="e66a7-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e66a7-134">NOTES</span></span>

## <span data-ttu-id="e66a7-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e66a7-135">RELATED LINKS</span></span>
