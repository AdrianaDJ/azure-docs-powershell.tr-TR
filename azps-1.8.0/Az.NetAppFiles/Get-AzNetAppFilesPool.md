---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: 8a85f3dff99184be984a7b08c7a4cafe25c697d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760782"
---
# <span data-ttu-id="24910-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="24910-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="24910-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24910-102">SYNOPSIS</span></span>
<span data-ttu-id="24910-103">Bir Azure NetApp dosyaları (ANF) havuzunun ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="24910-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="24910-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24910-104">SYNTAX</span></span>

### <span data-ttu-id="24910-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="24910-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24910-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="24910-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24910-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24910-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24910-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="24910-108">DESCRIPTION</span></span>
<span data-ttu-id="24910-109">**Get-AzNetAppFilesPool** cmdlet 'i ANF havuzunun ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="24910-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="24910-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24910-110">EXAMPLES</span></span>

### <span data-ttu-id="24910-111">Örnek 1: ANF havuzu edinin</span><span class="sxs-lookup"><span data-stu-id="24910-111">Example 1: Get an ANF pool</span></span>
```
PS C:\>Get-AzAnfPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
ProvisioningState : Succeeded
```

<span data-ttu-id="24910-112">Bu komut, "MyAnfAccount" hesabından MyAnfPool adlı hesabı alır.</span><span class="sxs-lookup"><span data-stu-id="24910-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="24910-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24910-113">PARAMETERS</span></span>

### <span data-ttu-id="24910-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="24910-114">-AccountName</span></span>
<span data-ttu-id="24910-115">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="24910-115">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24910-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="24910-116">-AccountObject</span></span>
<span data-ttu-id="24910-117">Döndürülecek havuzu içeren hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="24910-117">The account object containing the pool to return</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24910-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24910-118">-DefaultProfile</span></span>
<span data-ttu-id="24910-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="24910-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24910-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="24910-120">-Name</span></span>
<span data-ttu-id="24910-121">ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="24910-121">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: PoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24910-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24910-122">-ResourceGroupName</span></span>
<span data-ttu-id="24910-123">ANF havuzunun kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="24910-123">The resource group of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24910-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="24910-124">-ResourceId</span></span>
<span data-ttu-id="24910-125">ANF havuzunun kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="24910-125">The resource id of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24910-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24910-126">CommonParameters</span></span>
<span data-ttu-id="24910-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24910-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="24910-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24910-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24910-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24910-129">INPUTS</span></span>

### <span data-ttu-id="24910-130">System. String</span><span class="sxs-lookup"><span data-stu-id="24910-130">System.String</span></span>

### <span data-ttu-id="24910-131">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="24910-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="24910-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24910-132">OUTPUTS</span></span>

### <span data-ttu-id="24910-133">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="24910-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="24910-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24910-134">NOTES</span></span>

## <span data-ttu-id="24910-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24910-135">RELATED LINKS</span></span>