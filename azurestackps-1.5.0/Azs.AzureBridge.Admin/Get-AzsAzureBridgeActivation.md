---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 811a69b8d18c5e723702f73873188961f2739360
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2020
ms.locfileid: "93595239"
---
# <span data-ttu-id="7ffef-101">Get-AzsAzureBridgeActivation</span><span class="sxs-lookup"><span data-stu-id="7ffef-101">Get-AzsAzureBridgeActivation</span></span>

## <span data-ttu-id="7ffef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ffef-102">SYNOPSIS</span></span>
<span data-ttu-id="7ffef-103">Azure Köprüsü etkinleştirme 'yi döndürür.</span><span class="sxs-lookup"><span data-stu-id="7ffef-103">Returns the Azure Bridge Activation.</span></span>

## <span data-ttu-id="7ffef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ffef-104">SYNTAX</span></span>

### <span data-ttu-id="7ffef-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7ffef-105">List (Default)</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7ffef-106">Al</span><span class="sxs-lookup"><span data-stu-id="7ffef-106">Get</span></span>
```
Get-AzsAzureBridgeActivation -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="7ffef-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="7ffef-107">ResourceId</span></span>
```
Get-AzsAzureBridgeActivation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="7ffef-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ffef-108">DESCRIPTION</span></span>
<span data-ttu-id="7ffef-109">Azure yığını kaydedildikten sonra, etkinleştirme nesnesi Azure 'daki kayda bir Azure yığın dağıtımını bağlayan bilgileri (örneğin, kayıt son kullanım tarihi, ad vb.) içerir.</span><span class="sxs-lookup"><span data-stu-id="7ffef-109">Once Azure Stack has been registered, the activation object contains information that links an Azure Stack deployment to its registration in Azure, for example, the registration expiration date, name, etc.</span></span>

## <span data-ttu-id="7ffef-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ffef-110">EXAMPLES</span></span>

### <span data-ttu-id="7ffef-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7ffef-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName 'activationRG'
```

<span data-ttu-id="7ffef-112">"ActivationRG" kaynak grubunun altındaki Azure Bridge etkinleştirmeleri listesini alma</span><span class="sxs-lookup"><span data-stu-id="7ffef-112">Get a list of Azure Bridge Activations under the resource group "activationRG"</span></span>

### <span data-ttu-id="7ffef-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="7ffef-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeActivation -Name 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="7ffef-114">' ActivationRG ' altında ' Myacsyon ' adlı bir Azure köprü etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="7ffef-114">Get an Azure Bridge Activation by name 'myActivation' situated under 'activationRG'</span></span>

## <span data-ttu-id="7ffef-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ffef-115">PARAMETERS</span></span>

### <span data-ttu-id="7ffef-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="7ffef-116">-Name</span></span>
<span data-ttu-id="7ffef-117">Etkinleştirme adı.</span><span class="sxs-lookup"><span data-stu-id="7ffef-117">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ffef-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ffef-118">-ResourceGroupName</span></span>
<span data-ttu-id="7ffef-119">Azure yığınının kaydı sırasında kullanılan kaynak grubu; Ayrıca, portalda kaynak grubu adlarını da görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7ffef-119">The Resource Group used during the registration of Azure Stack; you can also view Resource Group names in the portal.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ffef-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7ffef-120">-ResourceId</span></span>
<span data-ttu-id="7ffef-121">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="7ffef-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ffef-122">-Atla</span><span class="sxs-lookup"><span data-stu-id="7ffef-122">-Skip</span></span>
<span data-ttu-id="7ffef-123">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="7ffef-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ffef-124">-Üst</span><span class="sxs-lookup"><span data-stu-id="7ffef-124">-Top</span></span>
<span data-ttu-id="7ffef-125">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="7ffef-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7ffef-126">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="7ffef-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ffef-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ffef-127">CommonParameters</span></span>
<span data-ttu-id="7ffef-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ffef-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ffef-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ffef-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ffef-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ffef-130">INPUTS</span></span>

## <span data-ttu-id="7ffef-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ffef-131">OUTPUTS</span></span>

### <span data-ttu-id="7ffef-132">Microsoft. AzureStack. Management. AzureBridge. admin. modeller. ActivationResource</span><span class="sxs-lookup"><span data-stu-id="7ffef-132">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ActivationResource</span></span>

## <span data-ttu-id="7ffef-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ffef-133">NOTES</span></span>

## <span data-ttu-id="7ffef-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ffef-134">RELATED LINKS</span></span>

